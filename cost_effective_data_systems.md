# Bojangles Front-Line Device: U.S.-Designed Data Systems, Microprocessors, and TSMC Manufacturing Integration

## Executive Summary

The front-line buffet device described in the preceding engineering specification requires more than stainless steel and heating elements. It requires a **data and control layer**—microprocessors, sensors, communication modules, and cloud-connected logic—that transforms a passive holding unit into an intelligent, self-monitoring, compliance-documenting piece of equipment. This document specifies that layer. The design philosophy is deliberate: **U.S.-based engineering firms design the data systems and select the microprocessors; TSMC's Arizona facility manufactures the silicon; the Chinese equipment manufacturer integrates the completed boards and sensors into the stainless steel housing.** This division of labor leverages American expertise in embedded systems and food safety compliance, Taiwanese semiconductor manufacturing capacity now operating on U.S. soil, and Chinese cost efficiency in metal fabrication and final assembly. The result is a device that meets NSF and FDA requirements, generates HACCP-compliant digital logs automatically, and provides Bojangles corporate with real-time visibility into every holding unit across the system.

---

## Part One: The Data System Architecture—What the Device Must Sense, Log, and Transmit

### 1.1 The Regulatory Mandate for Digital Temperature Logging

The FDA Food Code requires that hot-held time/temperature control for safety (TCS) foods be maintained at **135°F (57°C) or above** . The Code also requires that food safety records be kept and made available to regulators upon request. Traditional paper logs are vulnerable to falsification, loss, and human error—a problem that food safety auditors consistently identify as a systemic weakness. The front-line device addresses this by making **every temperature reading automatic, time-stamped, and tamper-proof**. The device does not ask the employee to remember to check the temperature; the device checks it continuously and logs the result without human intervention.

The data architecture must satisfy three requirements. First, **continuous monitoring**: temperature readings from each heating zone and each product probe at intervals of no more than five minutes. Second, **real-time alerting**: when a temperature drifts outside the safe band (below 135°F or above 180°F for sides; below 130°F or above 165°F for the steak zone), the system must notify the store manager and, if configured, the district manager, within sixty seconds. Third, **audit-ready records**: the logs must be stored in a format that is exportable, searchable, and admissible in a health inspection, with a retention period of at least ninety days on-site and two years in the cloud.

### 1.2 The Sensor Layer—What Must Be Measured

The front-line device requires four categories of sensors, each with specific placement and accuracy requirements.

**Temperature sensors** are the most critical. Each heating zone (sides and steak) requires a **primary control sensor** positioned in the water bath or directly adjacent to the heating element, and a **product probe** positioned in the food pan itself, ideally in the geometric center of the pan at the coldest point. The control sensor maintains the set point; the product probe verifies that the food—not just the air or the water—is at the safe temperature. The product probe must be **sanitary, food-grade, and removable for cleaning**, with a quick-disconnect fitting that does not require tools. The accuracy requirement is ±1°F for the product probe and ±2°F for the control sensor.

**Water level sensors** are required for the wet-operation water bath. A **float switch or a conductivity probe** detects when the water level falls below the safe minimum. When the level is low, the heating element must shut off automatically to prevent scorching and fire risk. The sensor must be resistant to scale buildup and easy to descale during routine maintenance.

**Door or access sensors** detect when the sneeze guard is opened or when a pan is removed. This data serves two purposes: it allows the system to infer when a pan has been swapped (triggering a hold-timer reset for the new product) and it provides a record of access for security and sanitation auditing.

**Power monitoring sensors** detect whether the device is receiving power and whether the heating elements are drawing current. A device that is plugged in but not heating is a device that will fail a health inspection; the power monitor catches this condition before the food temperature drops.

### 1.3 The Communication Layer—How Data Leaves the Device

The front-line device should support **three communication paths**, with automatic failover between them. The primary path is **Ethernet** where a wired connection is available—this is the most reliable and secure option for a fixed installation. The secondary path is **Wi-Fi (802.11ac or newer)** using the store's existing network infrastructure, with WPA3 encryption and a dedicated VLAN for equipment traffic to isolate it from customer Wi-Fi and POS systems. The tertiary path is **cellular (LTE Cat-M1 or NB-IoT)**, which provides connectivity even if the store's network is down or if the device is installed in a location where wired or Wi-Fi connectivity is impractical.

The communication module should be a **pre-certified module** rather than a discrete design, to simplify FCC certification and reduce development risk. Silicon Labs, a U.S.-based semiconductor company headquartered in Austin, Texas, offers wireless SoCs and modules supporting Wi-Fi, Bluetooth, Zigbee, Thread, and proprietary sub-GHz protocols . Their modules are pre-certified for FCC and can be integrated into the device's control board with minimal additional testing. The data should be transmitted using **MQTT over TLS** or a comparable lightweight, secure protocol, with the device authenticating to the cloud using a unique certificate stored in a secure element.

### 1.4 The Cloud and Dashboard Layer

The cloud platform receives the sensor data, stores it in a time-series database, and presents it through two interfaces: a **store-level dashboard** accessible on a tablet or the device's own touchscreen, and a **corporate dashboard** accessible to Bojangles operations and food safety teams. The store dashboard shows the current temperature of each zone, the hold time remaining for each pan, and any active alerts. The corporate dashboard aggregates data across all stores, identifies stores with chronic temperature deviations, and generates compliance reports that can be exported for health inspections.

The cloud platform must be **HACCP-compliant** and support **FDA 21 CFR Part 11** requirements for electronic records, including audit trails, user authentication, and data integrity controls. Commercial platforms such as myDevices provide this capability, with wireless sensors that log data to the cloud and generate HACCP-compliant digital logs that are time-stamped and tamper-proof . The device can either integrate with such a platform through an API or use a Bojangles-specific implementation. The advantage of a commercial platform is faster deployment and proven compliance; the advantage of a custom implementation is tighter integration with Bojangles' existing POS and inventory systems.

---

## Part Two: The Microprocessor Selection—U.S.-Designed Silicon for Embedded Control

### 2.1 The Control Board Architecture

The front-line device's control board is a **single-board computer or a microcontroller-based design** that performs four functions: reading sensors, executing the control logic (thermostat, hold timers, alerts), communicating with the cloud, and driving the local touchscreen display. The processing requirements are modest: a 32-bit microcontroller running at 50 to 150 MHz with 256 KB to 1 MB of flash memory and 64 to 256 KB of RAM is sufficient. The device does not need an application processor, a GPU, or advanced AI acceleration. It needs **reliability, low power consumption, industrial temperature range, and long-term availability**.

### 2.2 Candidate Microprocessors from U.S. Companies

Several U.S.-headquartered semiconductor companies manufacture microcontrollers suitable for this application. **Silicon Labs** (Austin, Texas) offers the EFM32 (32-bit ARM Cortex-M) and EFM8 (8-bit 8051-based) families, designed for low-power embedded applications with integrated analog peripherals, communication interfaces, and security features . The EFM32 is particularly well-suited to battery-backed or low-power applications, though the front-line device has mains power and does not require extreme low-power operation. The EFM8 is adequate for simpler control tasks but lacks the processing headroom for a graphical touchscreen interface.

**Texas Instruments** (Dallas, Texas) offers the MSP430 and SimpleLink families, both widely used in industrial and commercial equipment. The MSP430 is a 16-bit ultra-low-power MCU with a long track record in harsh environments. The SimpleLink family includes wireless MCUs with integrated Wi-Fi and Bluetooth, which could simplify the communication layer by eliminating the need for a separate wireless module. TI's MCUs are available in industrial temperature grades (-40°C to 125°C) and have long product lifecycles, which is important for equipment that will be installed in restaurants and maintained for a decade or more .

**NXP Semiconductors** (Eindhoven, Netherlands, with significant U.S. operations and design centers) offers the LPC800 and LPC5500 series, which are Cortex-M0+ and Cortex-M33 based MCUs designed for cost-sensitive embedded applications. The LPC800 series includes variants with operating temperatures up to 105°C and integrated ADC, DAC, and comparators—sufficient for sensor reading and control . NXP's LPC5500 series adds security features (SRAM PUF, secure boot) that may be valuable for protecting the device's firmware and communication credentials.

### 2.3 The Recommended Microprocessor: Silicon Labs EFM32 or TI SimpleLink

For the front-line device, the recommended microprocessor is the **Silicon Labs EFM32PG or EFM32GG** series, or the **TI SimpleLink CC3235** if integrated Wi-Fi is preferred. The EFM32 offers the best balance of low power, integrated analog peripherals, security features (Secure Vault for key storage), and long-term availability. The SimpleLink CC3235 integrates a Wi-Fi transceiver and a Cortex-M4 application processor on a single die, which simplifies the board design and reduces the component count. Both are U.S.-designed and available through distribution channels with industrial temperature ratings.

The microprocessor selection has implications for the manufacturing location. These MCUs are fabricated on **40nm or 28nm process nodes**, which are mature, high-volume processes . TSMC's Arizona Fab 21 began high-volume production of 4nm chips in Q4 2024 and is expanding to 3nm and 2nm . However, **MCUs are typically fabricated on older, mature nodes**, not the leading-edge nodes that TSMC Arizona is currently focused on. The 40nm and 28nm processes that produce these MCUs are more likely to run in TSMC's Taiwan fabs or in other foundries (GlobalFoundries, UMC, SMIC) than in Arizona. This is an important distinction: **TSMC Arizona is a leading-edge fab, not a mature-node fab**. If Bojangles requires that the microprocessor itself be fabricated in the United States, the options are more limited and may require selecting a U.S.-fabricated MCU from a different foundry.

---

## Part Three: TSMC Arizona—What It Can and Cannot Provide

### 3.1 Current Capabilities at Fab 21

TSMC's Arizona facility, Fab 21, is a **leading-edge semiconductor manufacturing complex** in north Phoenix. Its first fab began high-volume production of **4nm (N4) chips** in Q4 2024, and it is producing chips for Apple, AMD, and Nvidia . A second fab is targeted for **3nm (N3) production in the second half of 2027**, and a third fab for **2nm and A16 production** by the end of the decade . TSMC has committed $65 billion to the Arizona project and has received $6.6 billion in CHIPS Act funding .

The significance of this for Bojangles is **not that the front-line device's MCU will be made in Arizona**. It almost certainly will not be. MCUs for embedded control applications are fabricated on mature nodes (40nm, 28nm, or larger), and TSMC Arizona is not producing these nodes. What TSMC Arizona provides is a **proof point**: the United States now has leading-edge semiconductor manufacturing capacity on American soil, operated by a company with a track record of quality and reliability. If Bojangles' engineering department designs a more advanced control board in the future—perhaps one with integrated AI for predictive maintenance or vision-based quality inspection—the silicon for that board could plausibly come from Arizona. For the current device, the MCU will come from Taiwan or another foundry, and this should be acknowledged honestly in the engineering documentation.

### 3.2 The "Designed in USA, Manufactured by TSMC" Claim

The phrase "designed and manufactured in the USA, TSMC" is partially accurate and partially aspirational. The **design** of the control board, the firmware, the data architecture, and the cloud platform can and should be U.S.-based. The **microprocessor** is designed by a U.S. company (Silicon Labs or TI) but fabricated by TSMC in Taiwan or another foundry. The **final assembly** of the control board and the stainless steel housing will likely occur in China. The honest claim is: **"Engineered in the United States. Microprocessor designed in the United States. Silicon fabricated by TSMC. Equipment assembled by our manufacturing partner."** This is a supply chain reality that Bojangles should be transparent about, because customers and regulators increasingly care about provenance, and a false claim of domestic manufacturing is worse than an honest claim of global sourcing.

If Bojangles wants to maximize the U.S. content of the device, the following steps are feasible. First, specify **U.S.-designed MCUs** (Silicon Labs, TI, NXP) rather than Asian or European alternatives. Second, specify **U.S.-made sensors** where available (ThermoWorks, for example, is a U.S. company that manufactures temperature measurement equipment and offers connected HACCP tools ). Third, specify **U.S.-assembled control boards**—there are contract electronics manufacturers in the United States that can populate and test the boards, though at a higher cost than Chinese assembly. Fourth, specify **U.S.-hosted cloud infrastructure** (AWS, Azure, or Google Cloud) for the data platform. The stainless steel fabrication and final assembly will remain in China for cost reasons, but the intelligence of the device—the part that makes it more than a metal box—can be substantially American.

---

## Part Four: Integration—How the Data System Plugs into the Front-Line Device and the Broader Bojangles System

### 4.1 Physical Integration

The control board is mounted in the **electrical enclosure** described in the manufacturing specification, alongside the relay modules, power supply, and terminal blocks. The board connects to the sensors via **shielded cable** to prevent electrical interference from the heating elements. The temperature probes use **RTD or thermocouple** sensors with a **MAX31865 or MAX6675** interface chip on the board, which converts the analog signal to a digital value that the MCU can read. The water level sensor, door sensor, and power monitor connect to **digital input pins** on the MCU, with optoisolation to protect the MCU from voltage spikes.

The touchscreen display is a **7- to 10-inch capacitive panel** connected to the MCU via **SPI or parallel interface**. The display shows the zone temperatures, hold timers, and alert messages. The display is the employee's primary interface with the device, and it must be readable in a commercial kitchen environment—bright enough to be seen under fluorescent lighting, responsive enough to be used with gloves, and sealed to IP65 or better to withstand cleaning.

### 4.2 Data Integration with Bojangles Systems

The front-line device's data should flow into three Bojangles systems. First, the **POS system** receives a signal when a pan is swapped or when a product is running low, which can trigger a replenishment alert in the kitchen. Second, the **inventory system** receives consumption data inferred from pan swaps and hold-time discards, which improves forecasting and reduces waste. Third, the **food safety compliance system** receives the temperature logs and alert history, which generates the HACCP records that the store manager reviews and signs digitally.

The integration is achieved through **APIs** rather than direct database connections, for security and maintainability. The device publishes data to a **message broker** (MQTT or Kafka), and the Bojangles integration layer subscribes to the relevant topics and routes the data to the appropriate systems. This architecture decouples the device from the back-end systems, so that a change in the POS system does not require a firmware update on every device.

### 4.3 The Employee Interface—What the Data System Enables

The data system transforms the employee's interaction with the device from **reactive to proactive**. Without the data system, the employee checks the temperature when they remember to, replaces pans when they look empty, and discards food when the hold timer on a paper log expires. With the data system, the device tells the employee exactly what to do and when to do it. The touchscreen displays a **green, amber, or red status** for each pan: green means the product is within temperature and hold-time limits; amber means the hold time is approaching its limit and the pan should be swapped soon; red means the product has exceeded its limit and must be discarded. The employee does not need to remember the hold times or check the thermometer; the device does it for them.

The data system also enables **remote support**. If a heating element fails or a sensor drifts out of calibration, the cloud platform detects the anomaly and generates a service ticket before the store manager notices a problem. The service technician arrives with the correct replacement part and the device's service history, reducing downtime and repair cost. This is the same principle behind Middleby's Open Kitchen platform, which monitors temperatures, provides real-time alerts, and helps operators prioritize repairs and equipment replacements . The front-line device should adopt this model: the data is not just for compliance; it is for **operational efficiency and equipment uptime**.

---

## Conclusion

The front-line buffet device is a stainless steel box with heating elements, but its value—to Bojangles, to the store operator, and to the health inspector—lies in the data it generates and the intelligence it applies to that data. The U.S.-designed microprocessor, the U.S.-engineered firmware and cloud platform, and the TSMC-fabricated silicon (even if that silicon is on a mature node in Taiwan rather than a leading-edge node in Arizona) form a control layer that makes the device **self-monitoring, self-documenting, and self-diagnosing**. The Chinese manufacturing partner integrates this control layer into the metal housing, and the resulting device is greater than the sum of its parts. It is a piece of equipment that does not just hold food at a temperature; it holds food at a temperature **and proves that it did so**, every minute of every shift, in a format that satisfies the FDA, the local health department, and the Bojangles quality assurance team. The Main Ingredient Test applies: does this data system make the sides hotter, the holding more reliable, or the compliance more certain? A device that knows its own temperature and reports it honestly does all three. A device that relies on a human to remember to check a thermometer does none of them reliably. The data system is not an accessory. It is the difference between a holding unit and a **managed holding unit**.

---

**APPENDIX: DATA SYSTEM COMPONENT SUMMARY**

| Component | Specification | U.S. Content | Manufacturing Location |
|-----------|--------------|--------------|----------------------|
| Microprocessor | Silicon Labs EFM32PG or TI SimpleLink CC3235, 32-bit, industrial temp | Designed in USA | TSMC Taiwan (mature node) |
| Temperature sensors | RTD or thermocouple, ±1°F, sanitary probe | ThermoWorks or equivalent (USA) | Sensor element may be imported |
| Wireless module | Pre-certified Wi-Fi/LTE module | Silicon Labs (USA) | Module assembled in Asia |
| Control board | 4-layer PCB with MCU, sensor interfaces, relays | Designed in USA | Assembled in China (contract manufacturer) |
| Touchscreen | 7–10 inch capacitive, IP65, glove-compatible | Designed in USA | Assembled in Asia |
| Cloud platform | MQTT/TLS, time-series database, HACCP-compliant | AWS/Azure (USA) | U.S. data centers |
| Enclosure integration | Mounted in NEMA 4 electrical enclosure | — | China (Jiekexun or equivalent) |
