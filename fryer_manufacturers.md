# Production Plan: Integrated Frying System for Bojangles

## A Letter to Prospective Manufacturers

**To the Commercial Frying Equipment Manufacturers of North America:**

Bojangles is seeking a manufacturing partner—or a coordinated group of partners—to produce an integrated frying system that will serve as the engine of our back-of-house automation plan. This is not a request for a standard catalog fryer. It is a specification for a system that must fry our bone-in chicken and country fried steak to the standards our customers have trusted since 1977, manage its own oil from delivery to disposal, and deliver finished product to the service station in a condition that preserves the crust our brand is known for.

We are approaching this project with clear eyes about what we do and do not know. We know our chicken: a twelve-hour buttermilk marinade, a double dredge in seasoned flour, and a fry at approximately 350°F to 360°F until the internal temperature reaches 165°F. We know our breading station: a custom refrigerated table that holds product safely for six continuous hours of service, built by Beverage-Air to our specifications because no off-the-shelf unit could meet the demand. We know our oil: it must be clean, filtered, and maintained at the correct level to produce the golden, craggy crust that customers recognize.

What we need from you is the machine that brings these elements together—a frying system that is not merely a vat of hot oil, but a coordinated subsystem that interfaces with our data platform, our holding-time management system, and our service-line delivery workflow. The sections that follow specify our requirements in detail. We invite your engineering team to respond with a proposal that addresses every point, and we commit to an open dialogue about what is achievable, what is not, and what compromises will best serve the customer who eats the chicken.

---

## Part One: Physical and Capacity Specifications

### 1.1 Footprint and Configuration

The frying system must fit within the back-of-house footprint of a standard Bojangles restaurant, including both existing stores undergoing retrofit and new builds. The recommended configuration is a **dual-vat open fryer battery** with independent vat control, allowing one vat to be filtered or cleaned while the other continues cooking. This "filter while cooking" capability is non-negotiable for a high-volume breakfast and lunch operation where stopping all frying for filtration is operationally unacceptable.

The system footprint should not exceed **48 inches in width, 32 inches in depth, and 46 inches in height**, excluding the exhaust hood connection. This aligns with the dimensions of commercial open fryers from Henny Penny and Frymaster that are already proven in QSR environments. If the manufacturer proposes a larger configuration, the proposal must include a floor plan showing how the unit fits within a standard Bojangles kitchen and how it interfaces with the breading table, the holding station, and the service-line transfer point.

### 1.2 Oil Capacity and Production Throughput

The oil capacity per vat should be in the **30 to 40 pound range**, which represents the current efficiency standard in the industry. Frymaster's FilterQuick 30 uses 30 pounds per vat while delivering full-size frying performance, consuming 40% less oil than traditional 50-pound models. Henny Penny's Evolution Elite similarly uses 40% less oil than standard tanks while cooking the same load size. Bojangles does not need larger vats; we need vats that recover temperature quickly and maintain it under load.

Production throughput must support a peak demand of **approximately 120 to 140 pounds of finished product per hour** across the battery. This estimate is based on a high-volume breakfast rush where bone-in chicken, tenders, and country fried steak are fried simultaneously. The manufacturer should specify the recovery time (the time required to return to set temperature after a basket load) and the maximum batch size for each product type. A recovery time exceeding three minutes is unacceptable for our operation, because it would create a bottleneck during peak periods.

### 1.3 Construction Materials

All food-contact surfaces must be **304 stainless steel**, with the frypot, door, and cabinet sides in stainless steel for durability and cleanability. The heating elements must be of a design that is accessible from the front of the unit for service and replacement without moving the fryer. The unit must be mounted on **heavy-duty casters** with locking brakes, allowing it to be moved for cleaning and repositioned securely during operation.

---

## Part Two: Software and Control Requirements for Bojangles

### 2.1 The Bojangles Cooking Program Library

The fryer's controller must support a **dedicated Bojangles program library** that is locked to our specifications and cannot be inadvertently altered by store-level employees. This library should include, at minimum, the following programs:

| Program Name | Product | Oil Temperature | Cook Time | Notes |
|-------------|---------|----------------|-----------|-------|
| BJ-BoneIn-Dark | Legs, thighs | 325°F | Per piece size (programmed by weight range) | Lower temp for dark meat to ensure interior doneness |
| BJ-BoneIn-White | Breasts, wings | 340°F | Per piece size | Higher temp for white meat to prevent drying |
| BJ-Tenders | Chicken tenders | 350°F | 5–6 minutes | Based on Bojangles' tender specifications |
| BJ-CFS | Country fried steak | 350°F | Per patty thickness | Breading must remain intact; no floating |
| BJ-LTO | Limited-time offerings | Programmable | Programmable | Empty slots for seasonal items |

The controller must allow corporate engineering to **push program updates remotely** through the Bojangles data platform, without requiring a service technician to visit each store. This capability is essential for launching limited-time products across the system without a labor-intensive manual rollout.

### 2.2 Interface with the Bojangles Data Platform

The fryer controller must expose a **secure API** (REST or MQTT) that publishes the following data to the Bojangles cloud platform at intervals of no more than five minutes:

- Oil temperature per vat (set point and actual)
- Oil quality indicator (if an oil quality sensor is installed)
- Filtration cycle count and last filtration timestamp
- Oil level status (normal, low, critical)
- Batch counts per program (for demand forecasting)
- Energy consumption per vat (if a current transformer is installed)
- Fault codes and alert history

The controller must also **accept commands** from the platform, including program updates, filtration initiation, and diagnostic queries. The API must be documented in full, with example payloads, so that Bojangles' engineering team can integrate the fryer into the existing dashboard without reverse-engineering proprietary protocols.

### 2.3 Employee Interface

The fryer's local interface must be a **touchscreen controller** that is readable under commercial kitchen lighting, responsive to gloved hands, and sealed to IP65 or better for cleaning. The interface should display, at minimum: the active program for each vat, the time remaining on the current batch, the oil temperature, and any active alerts. The interface must be **icon-driven with minimal text**, consistent with the multilingual workforce in Bojangles kitchens. A physical **emergency stop button** must be provided on the front of the unit, within easy reach, that cuts power to all heating elements and basket lifts.

---

## Part Three: Automation Specifications

### 3.1 Automatic Filtration

The system must include **built-in automatic filtration** that can be initiated by the employee with a single button press, or automatically at preset intervals based on cook cycle counts. The filtration cycle should complete in **under four minutes per vat**, during which the other vat remains available for cooking. The filtration system must include a **rear oil flush** to clear sediment from the drain path, and a **filter pan** that is accessible from the front of the unit for cleaning without moving the fryer.

The filtration system must be designed so that the oil returns to the vat at the correct temperature, ready for the next batch. Henny Penny's Smart Touch Filtration returns hot filtered oil in less than four minutes. This performance standard is the benchmark Bojangles expects.

### 3.2 Automatic Oil Top-Off (ATO)

The system must include an **automatic top-off** function that monitors oil level and replenishes from a **Jug-in-Box (JIB)** or bulk oil connection as needed. The JIB should be located inside the fryer cabinet for convenience and protection. The ATO system must log top-off events to the data platform, allowing corporate engineering to correlate oil consumption with batch volume and identify stores with abnormally high oil usage. The system should alert the store when the JIB is below 20% capacity, providing sufficient warning to order replacement before the fryer runs dry.

### 3.3 Oil Quality Monitoring

Bojangles requires the fryer to support an **oil quality sensor** that provides real-time indication of oil degradation. The Frymaster FilterQuick 30 offers an optional Oil Quality Sensor (OQS) that monitors oil health and signals when oil should be changed. This capability transforms oil management from a schedule-based exercise (change oil every X days) to a condition-based exercise (change oil when it actually needs changing), which reduces waste and prevents the use of degraded oil that would compromise product quality.

The oil quality data must be published to the Bojangles platform, where it can be aggregated across stores to identify patterns. A store that consistently reaches end-of-life oil sooner than comparable stores may have a filtration problem, a temperature calibration issue, or a product mix that accelerates degradation.

### 3.4 Waste Oil Disposal Interface

The fryer must include a **waste oil discharge pump and connection point** that allows used oil to be pumped directly to an external storage tank or recycling container. This eliminates the manual handling of hot oil, which is a leading cause of kitchen burns. The connection point should be compatible with the equipment used by Bojangles' waste oil recycling partners, such as DAR PRO Solutions or Restaurant Technologies, both of which offer direct fryer connections and nationwide collection services.

The discharge system must be **interlocked** so that it cannot operate while the vat is at cooking temperature unless the operator has explicitly initiated a disposal cycle. The system should also log disposal events, providing a record that can be used to verify compliance with local regulations and to reconcile waste oil volumes with fresh oil purchases.

### 3.5 Product Delivery to Service Station

The fryer must include a **basket lift mechanism** that raises the basket at the end of the cook cycle and holds it above the oil, allowing excess oil to drain before the product is removed. This is a standard feature on commercial fryers and is essential for preventing greasy product. The basket lift should be programmable to a **dwell time** (typically 15 to 30 seconds) before the basket is fully raised, allowing the product to drain without cooling excessively.

For delivery to the service station, the recommended configuration is a **heated transfer cart** that docks with the fryer and receives finished product directly from the basket lift. The cart maintains product at 150°F to 160°F and is vented to allow steam escape, preserving crust crispness during the short transit to the service line. The cart should be designed to interface with the holding-time management system: when product is loaded, a timer starts, and the service-line holding unit displays the remaining hold window.

---

## Part Four: Cooking Process and Operational Workflow

### 4.1 The Bojangles Cooking Sequence

The fryer is the final step in a process that begins twelve hours before the product reaches the oil. The chicken is marinated in buttermilk, hot sauce, and salt for twelve hours in a commercial tumbler, which tenderizes the meat and infuses flavor throughout. The chicken is then dredged in seasoned self-rising flour, dipped in a wet mixture of eggs and milk, and dredged again—the double dredge that creates the thick, craggy crust Bojangles is known for. The breaded product rests on a rack for at least ten to fifteen minutes before frying, allowing the coating to hydrate and adhere.

The fryer operator's role is to **load the basket, select the program, and respond to alerts**. The operator does not time the cook or judge doneness by sight; the fryer's controller does that. When the program is complete, the basket lift raises automatically, and the operator transfers the product to the heated transfer cart. The operator then confirms the transfer on the touchscreen, which starts the hold timer and logs the batch in the data platform.

### 4.2 Temperature and Time Specifications

Based on Bojangles' established process and industry-standard frying practice, the following specifications apply:

- **Bone-in dark meat (legs, thighs):** 325°F, cook time determined by piece weight, internal temperature target 175°F for dark meat.
- **Bone-in white meat (breasts, wings):** 340°F, cook time determined by piece weight, internal temperature target 165°F.
- **Tenders:** 350°F, 5 to 6 minutes, internal temperature 165°F.
- **Country fried steak:** 350°F, cook time determined by patty thickness, internal temperature 165°F.

The fryer controller must allow these specifications to be adjusted by corporate engineering based on product testing, but the store-level operator must not have the ability to alter them. The program library is locked; only the corporate platform can push changes.

### 4.3 Filtration and Oil Management Workflow

Filtration should occur **at least every four to six cook cycles**, or more frequently if the oil quality sensor indicates degradation. The fryer controller tracks cook cycles and prompts the operator to filter when the threshold is reached. The operator initiates filtration with a single button press, and the system executes the drain, flush, and return sequence automatically. During filtration of one vat, the other vat remains available for cooking, so the operation is not interrupted.

The JIB should be checked at the start of each shift, and the fryer will alert when the level falls below 20%. When the JIB is empty, the operator replaces it with a fresh box from storage. The empty box is returned for recycling. Waste oil disposal should occur at the end of each day or when the oil quality sensor indicates end-of-life, using the discharge pump to transfer oil to the external storage tank.

---

## Part Five: Response Requirements and Next Steps

Bojangles requests that interested manufacturers respond to this production plan with a proposal that includes:

1. **A specific model or configuration** that meets the specifications in Parts One through Four, with a dimensioned drawing and a bill of materials.
2. **A software integration plan** describing how the fryer's controller will expose the required data and accept the required commands, including a sample API specification.
3. **A certification timeline** for NSF/ANSI 4 (hot food holding and cooking equipment) and UL/ETL listing, if the proposed model is not already certified for the U.S. market.
4. **A prototype and pilot plan**, including the cost and lead time for building a single unit for Bojangles' testing and evaluation.
5. **A pricing schedule** for volume production, with a clear breakdown of the base unit, the automation options, and the software integration work.

Bojangles will evaluate proposals based on three criteria, in order of priority: **does the system produce chicken that meets our taste and texture standards; does the automation genuinely reduce labor and improve consistency; and is the total cost of ownership—including energy, oil, water, and maintenance—lower than the current baseline.** The Main Ingredient Test applies: if the system makes the chicken more flavorful, the crust more consistent, or the operation more affordable, it belongs. If it merely makes the fryer more expensive, it does not.

We look forward to your response. The chicken that comes out of your machine will be eaten by millions of people who expect it to taste like Bojangles. That is the standard. We will not compromise it.

**Sincerely,**

**Bojangles Corporate Engineering Department**

---

**Appendix: Summary of Key Requirements**

| Category | Requirement |
|----------|-------------|
| Configuration | Dual-vat open fryer, independent control |
| Footprint | ≤ 48" W × 32" D × 46" H |
| Oil capacity | 30–40 lbs per vat |
| Throughput | 120–140 lbs finished product per hour |
| Materials | 304 stainless steel food zone |
| Programs | Locked Bojangles library, remote push capability |
| Data | Secure API, 5-minute interval, full documentation |
| Filtration | Automatic, <4 min per vat, filter-while-cooking |
| Top-off | Automatic, JIB or bulk, level alerts |
| Oil quality | Optional sensor, data to platform |
| Disposal | Pump and connection for external recycling |
| Delivery | Basket lift with dwell, heated transfer cart interface |
| Certification | NSF/ANSI 4, UL/ETL listed for U.S. |

