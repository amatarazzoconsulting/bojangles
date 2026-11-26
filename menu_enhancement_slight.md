# **Bojangles Automated Gravy Production Machine**

## **Technical design specification, manufacturing proposal, and supplier development plan**

### **1. Project objective**

The proposed machine is a commercial automated gravy preparation and dispensing appliance designed for high-volume restaurant kitchens. Its purpose is to prepare several varieties of gravy from standardized, replaceable ingredient cartridges, using a metered potable-water connection, automated mixing, controlled heating, and direct delivery into a heated serving pan.

The appliance should eliminate much of the repetitive manual work associated with measuring dry ingredients, mixing, cooking, and transferring gravy. It should also make it possible for restaurants to produce consistent gravy batches throughout the day.

The design is intended for commercial food-service use, not domestic kitchen use. It should be manufactured as a durable stainless-steel appliance with removable food-contact components, industrial controls, automated recipe management, and accessible sanitation systems.

The initial design should support five gravy varieties, with provision for expansion to eight cartridges without replacing the central mixing and heating system.

### **2. Proposed machine configuration**

The following dimensions establish a starting point for engineering drawings and prototype construction. They are preliminary design targets and should be confirmed by the mechanical engineer after component selection and production-volume testing.

| Assembly              | Preliminary specification                                                          |
| --------------------- | ---------------------------------------------------------------------------------- |
| Overall height        | 60 inches                                                                          |
| Overall width         | 30 inches                                                                          |
| Overall depth         | 32 inches                                                                          |
| Main frame            | Welded stainless-steel structure                                                   |
| Exterior panels       | 304 stainless steel                                                                |
| Food-contact surfaces | 304 stainless steel, with appropriate food-contact finishes                        |
| Cartridge capacity    | 5 standard cartridges                                                              |
| Expansion capacity    | 8 cartridges                                                                       |
| Mixing vessel         | 2-gallon nominal capacity                                                          |
| Normal batch sizes    | 1, 2, or 4 quarts                                                                  |
| Heating system        | Electrically controlled                                                            |
| Water supply          | Metered potable-water connection                                                   |
| Dispensing            | Sanitary, large-bore food-grade outlet                                             |
| User interface        | Industrial touchscreen                                                             |
| Power                 | Preliminary 208–240 V AC design; final rating determined by electrical engineering |
| Installation          | Commercial kitchen floor-standing appliance                                        |

The machine should be divided into five principal sections:

1. Upper ingredient cartridge compartment.
2. Central ingredient dosing and mixing compartment.
3. Lower heating and cooking compartment.
4. Front-facing dispensing and serving-pan compartment.
5. Rear or lower utility compartment containing electrical, water, pump, and control components.

This arrangement separates dry ingredient storage from wet processing and electrical equipment, while keeping the areas requiring frequent cleaning accessible to kitchen employees.

### **3. Ingredient cartridge assembly**

The cartridge assembly is one of the most important parts of the machine. It should be engineered as a modular inventory system in which each cartridge can be removed and replaced without opening the mixing chamber.

The initial configuration should include five individually identified cartridges:

| Cartridge | Product                            | Intended use                            |
| --------- | ---------------------------------- | --------------------------------------- |
| 1         | Southern sausage gravy formulation | Biscuits and breakfast service          |
| 2         | Black pepper gravy                 | Biscuits, chicken, and breakfast dishes |
| 3         | Brown country gravy                | Steak cutlets and entrées               |
| 4         | Chicken gravy                      | Chicken dishes and mashed potatoes      |
| 5         | Specialty gravy                    | Rotating menu or seasonal formulation   |

Each cartridge should be manufactured from food-compatible material and have a sealed ingredient compartment. A reusable cartridge housing with replaceable sealed ingredient bags is one possible approach. Another option is a disposable, prefilled cartridge designed for single-use replacement.

**Recommended cartridge design:**

- Approximate external dimensions: 5 inches wide × 8 inches deep × 12 inches tall.
- Replaceable sealed ingredient container.
- Mechanical locking interface.
- RFID or barcode identification.
- Moisture-resistant closure.
- Food-grade dispensing outlet.
- Internal agitator or vibration mechanism if needed to prevent powder bridging.
- Cartridge-level sensing or electronic inventory tracking.

These dimensions are an initial packaging envelope, not a final specification. The cartridge volume should be calculated from the bulk density and quantity of the selected gravy formulation.

A precision auger feeder should be installed below each cartridge. The auger should be driven by a small geared electric motor and should dispense the formulation into the mixing chamber at a controlled rate. Each feeder should be removable for cleaning and maintenance.

For accurate ingredient dosing, the machine should use a load cell or calibrated gravimetric measurement system. The controller should compare the measured quantity against the programmed recipe before proceeding.

### **4. Water metering and supply assembly**

The machine should connect to the restaurant's potable-water supply through a dedicated inlet. The inlet should include:

- Approved water shutoff valve.
- Backflow prevention appropriate to the installation.
- Replaceable sediment filtration where required.
- Food-service-compatible tubing and fittings.
- Pressure regulator if required by the selected components.
- Electrically controlled water inlet valve.
- Water flow meter.
- Independent maximum-fill sensor.

The machine should measure water by volume rather than relying on a timed valve opening alone.

A preliminary water-metering accuracy target is ±2% of the programmed quantity, subject to validation with the selected flow meter and operating water pressure.

The water should enter the mixing chamber through a spray or distribution manifold so that the dry ingredients are incorporated evenly. This helps reduce the formation of dry pockets and lumps.

The water system should be designed so that the potable-water supply cannot become contaminated by the gravy-processing system.

### **5. Mixing vessel and mechanical agitation**

The central mixing vessel should be constructed from food-grade 304 stainless steel. A nominal two-gallon vessel provides a practical starting point for producing batches of up to four quarts while allowing room for agitation and expansion.

The vessel should have a removable lid, smooth internal surfaces, rounded internal corners, and a bottom configuration that permits complete drainage.

**Recommended mixing components:**

- Variable-speed electric gear motor.
- Stainless-steel mixing shaft.
- Removable food-grade impeller.
- Mechanical shaft seal suitable for food processing.
- Vessel temperature sensor.
- Liquid-level sensor.
- Removable inspection cover.
- Bottom discharge valve.

The mixing mechanism should operate at multiple speeds. A lower speed should incorporate the powder into the water without excessive splashing. A higher speed should provide additional blending and help achieve a uniform consistency.

The initial engineering target could be a variable range of approximately 100–600 RPM. The actual operating range must be determined through tests using the selected gravy formulations, because excessive agitation can introduce air, affect texture, and create unnecessary mechanical wear.

A scraper-style mixing attachment may be necessary if testing shows that gravy sticks to the heated vessel walls. The scraper should be removable and made from a suitable food-contact material.

### **6. Heating and temperature control**

The heating system should cook the gravy directly in the mixing vessel or in a connected heated cooking vessel.

For the first prototype, I recommend a jacketed stainless-steel vessel with electric resistance heating. This provides more uniform heating than placing a conventional heating element directly in contact with thick gravy.

The heating assembly should include:

- Electrically controlled heating elements.
- Independent temperature sensors.
- Insulated vessel walls.
- Over-temperature protection.
- Low-liquid heating protection.
- Automatic heater shutdown.
- Temperature-controlled agitation.
- Removable service access.

The machine should use a programmable temperature controller with a separate independent safety cutoff. The normal operating temperature should be determined by the approved recipe and validated cooking procedure rather than by one universal setting for every gravy.

The control system should record the cooking temperature and duration for each batch. It should not release the product until the required recipe conditions have been achieved.

The cooking chamber and serving pan should have separate temperature controls. The cooking system prepares the gravy; the serving station maintains it at the required hot-holding temperature. In the United States, the FDA Food Code generally specifies 135°F (57°C) or above for hot-held time/temperature control for safety food, subject to applicable local rules and approved procedures.

### **7. Dispensing assembly and serving-pan station**

The completed gravy should be discharged into a removable stainless-steel serving pan.

The outlet should be designed for a thick, viscous food product. A wide-bore sanitary valve is preferable to a small-diameter tube, which could become obstructed by thick gravy or seasoning particles.

The outlet assembly should include:

- Food-grade sanitary valve.
- Removable transfer connection.
- Smooth internal passage.
- Drip-control mechanism.
- Accessible cleaning connection.
- Optional automatic portion control.

The serving-pan compartment should accommodate a standard commercial food-service pan where possible. The final pan dimensions should be selected after reviewing the restaurant's existing holding equipment.

A heated pan station should maintain the gravy at its approved hot-holding temperature. It should include a temperature sensor and a visible temperature display.

The machine should also have a low-level sensor or weight sensor to notify employees when the serving pan needs replenishment.

### **8. Control electronics and software**

The machine should use an industrial programmable logic controller (PLC) or equivalent industrial control platform. A separate touchscreen should provide the employee interface.

The controller should manage the complete production cycle:

1. Cartridge identification.
2. Recipe selection.
3. Water measurement.
4. Ingredient dispensing.
5. Mixing.
6. Heating.
7. Temperature verification.
8. Finished-product transfer.
9. Serving-pan monitoring.
10. Batch record storage.
11. Cleaning and maintenance alerts.

The touchscreen should display the selected gravy, batch size, ingredient quantity, water quantity, cooking progress, temperature, and remaining cartridge inventory.

The software should allow authorized management personnel to load or update recipes. Employees should be restricted to approved recipes and batch sizes.

The control system should also prevent unsafe operating conditions. For example, it should not allow heating when the vessel is empty, dispensing when the outlet is obstructed, or cartridge dosing when the mixing vessel is not ready.

The system should record the date, time, recipe, batch quantity, cartridge identification, and relevant temperature information for each production cycle.

## **8. Electrical, mechanical, and safety requirements**

The machine should be designed for commercial electrical service. A 208–240 V AC configuration is a reasonable starting point for a US commercial kitchen, but the final voltage, phase, amperage, and circuit requirements must be calculated from the heating load, motor ratings, pumps, and controls.

The electrical compartment should be separated from the food-processing area. It should contain:

- Industrial PLC controller.
- Motor speed controller.
- Heating-element contactors or solid-state power controls.
- Circuit protection and overload protection.
- Emergency-stop circuit.
- Grounding and bonding connections.
- Sealed cable entries appropriate for the cleaning environment.
- Temperature and water-level sensor connections.

The machine should include an emergency stop on the front panel. Opening a designated service panel should disable hazardous moving components. The mixing motor should not operate when the mixing vessel is open or when a maintenance interlock has been activated.

The design should also include protection against dry heating, overfilling, water leakage, motor overload, excessive pressure, and uncontrolled heating. The machine should not use a pressurized vessel unless pressure operation is specifically engineered, certified, and necessary for the process.

All electrical and food-contact components must be suitable for their intended commercial environment. The manufacturer should identify the applicable NSF/ANSI sanitation standards and UL or ETL electrical certification requirements before manufacturing. These certifications should be verified for the finished machine, not assumed from certificates belonging to individual components.

## **9. Recommended manufacturing construction**

The manufacturer should receive a complete engineering package before production begins. The package should include:

**Mechanical drawings**

- Front, rear, side, and top elevations.
- Internal assembly drawings.
- Cartridge docking and locking drawings.
- Mixing-vessel and impeller drawings.
- Heating-jacket drawings.
- Water and ingredient piping diagrams.
- Dispensing-valve assembly.
- Serving-pan dimensions.
- Electrical compartment and service-access drawings.

**Manufacturing materials**

- 304 stainless steel for the principal food-contact vessel and enclosure.
- 316 stainless steel where the ingredient chemistry or cleaning chemicals justify its use.
- Food-grade silicone or other suitable food-contact seals.
- Food-grade tubing and sanitary fittings.
- Corrosion-resistant fasteners in wet areas.
- Appropriate insulation around heated components.

**Manufacturing processes**

- CNC laser cutting for sheet-metal panels.
- Precision bending and forming.
- TIG welding for stainless-steel food-contact assemblies.
- Internal weld finishing and passivation as appropriate.
- CNC machining for shafts, impellers, and valve components.
- Electrical harness fabrication.
- PLC programming and touchscreen integration.
- Final assembly and functional testing.

The manufacturer should provide 3D CAD files, two-dimensional production drawings, a bill of materials, electrical schematics, software documentation, and a complete service-parts list. These deliverables should be part of the contract.

## **10. Manufacturers to approach**

For cost-effective manufacturing, I would investigate Chinese OEM/ODM factories that already produce commercial sauce cookers, jacketed kettles, mixing equipment, and automated food-processing machinery. These companies have relevant manufacturing capabilities, although none should be assumed to have an existing gravy cartridge machine identical to this design.

The most economical approach may be to commission one factory to build the stainless-steel and mechanical assemblies, while specifying the controls, sensors, motors, and safety components separately.

### **Potential Chinese manufacturing partners**

[Good Price New-Style Multi-Function Tomato Paste  Cooking Mixing Production Line - Juice /Dairy Cooking Equipment and Cooking Mixing Production Line](https://images.openai.com/static-rsc-4/q3M8Rs-fk4IIhdTslMmvd7mX6KKofP6gmyqwKVjOVfN3Y06mIkmQ-dcu0IPyYTte054FhxJ4XNaOBedWSte35b4sSSSKPW27G1pOlF_8zEyO1EAG_7iUm5WZsyisYcxk6NslvTRNO97_RySj84JU8beB4T-3yGCDQ54p2FEOOeI?purpose=inline)

**1. ZHUCHENG MBC Industrial & Trading Co., Ltd.**

Strong initial candidate

Located in Shandong, China. Its listed capabilities include industrial jacketed kettles, mixing cookers, sauce-processing machinery, and OEM/ODM customization. This makes it a logical company to approach about the mixing and heating system.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.sourcingai.com\&sz=32)

SourcingAI+2



Website and supplier information: [MBC manufacturer profile](https://chinambcfoodmachine.en.made-in-china.com/?utm_source=chatgpt.com)

[Longmai Commercial Jam Sauce Electric Jacket Kettle with Planetary - Cooking Kettle and Electric Jacketed Kettle](https://images.openai.com/static-rsc-4/Mt0f-QDA2DmCNBk0aoTGa4nliRXfes26Ea5ltyWLgd5G7j1RwWt5O9e3hO8vUlBb5QmiAUoTx7H99q3FHoUvebOvf1ENCIFrc7_S4vuzJs2Xnz6Ypl1JaQ6rhIjpzLmUb4-CU_KZVyL2OpXYcAGIkC4kAlw4-f_XrJd_DapSgH8?purpose=inline)

**2. Zhucheng Longmai Machinery Co., Ltd.**

Its published equipment information describes sauce and paste cooking machines with PLC control, adjustable mixing, heating options, and OEM/ODM customization. Ask whether it can engineer a smaller two-gallon machine rather than supplying its larger industrial models.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://longmaimachinery.en.made-in-china.com\&sz=32)

Made-in-china.com



Supplier listing: [Longmai Machinery profile](https://longmaimachinery.en.made-in-china.com/?utm_source=chatgpt.com)

[Large Capacity Gurry Chili Cooking Kettle Commercial Hot Sale Cooking Pot Mixer - Cooking Pot Mixer and Planetary Cooking Kettle Mixer](https://images.openai.com/static-rsc-4/RoA2lc1h3-U6RIJVUKr0gwiNPafxmutlEGrlKl8-NkC-b1oOzhx5KQg9I4KzXlB-0IcpviRlWydwtTGiDDBsROsuDw8jT707vMl52XQ8zQTmTa52C9LYLOSY-Ai6-jnA5B_eQx5cZbWQuJ3jWVTU1fidenXxk6hO1YyFgzNQSYg?purpose=inline)

**3. Zhucheng Chengchuan Machinery Co., Ltd.**

Its published product range includes automatic planetary mixing cookers, jacketed kettles, sauce equipment, and customized food-processing machinery. Ask about designing the cartridge-feeding system and compact dispensing assembly.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://sdccjx.en.made-in-china.com\&sz=32)

Zhucheng Chengchuan Machinery Co., Ltd.



Supplier profile: [Chengchuan Machinery profile](https://sdccjx.en.made-in-china.com/?utm_source=chatgpt.com)

### **Potential US manufacturing and engineering partners**

It may be worthwhile to have the first prototype engineered or reviewed in the United States, even if the production units are eventually manufactured in China. This provides a way to resolve food-safety, electrical, serviceability, and certification requirements before committing to a large overseas order.

[CUSTOM STAINLESS STEEL FABRICATION — ATLANTIC COAST RESTAURANT AND MECHANICAL SERVICES](https://images.openai.com/static-rsc-4/2_Wf8LR4Fl1vSg0t4WGO7JYda7_yJ7iVYXEJ2hI9A4tQNVb-9R5HTI0jXSrQBnXjBjYdHwRj3kIIg0NAiwrCldNsCgHb4twHunyChu9JDmIHDCUMsPDP3mOJe6i-7UK1X2rBqZSLtAWJHz5FvWvW7e5h7ATLiNutymB_iqd7GI0?purpose=inline)

**4. Babington Technology**

Offers custom commercial food-service equipment fabrication, design assistance, and contract manufacturing. Its published capabilities include precision stainless-steel fabrication and coordination of equipment production.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.babingtontechnology.com\&sz=32)

Babington Technology



[Babington Technology](https://www.babingtontechnology.com/?utm_source=chatgpt.com)

[Metal](https://images.openai.com/static-rsc-4/7Ib7w2HsduL_3jHkCcraKr7TAk2V1lPnHVTU0xF9PvsXQPY5u_4p1m3LY2z6QYYlaBNG5FR2xly8aqGr5qlkt0LhS5vM-V5QRfzYwpLQDtQQb4z8RWdjyPMjOGAbh53zVX-oIEW7Vy7flanT4lImSTT1Ntq4SczW4gOdf7lnoks?purpose=inline)

**5. HFI Manufacturing**

Works with restaurant-equipment OEMs and provides stainless-steel fabrication, prototyping support, and production manufacturing. Its experience with food-service equipment could make it useful for reviewing the enclosure and fabrication package.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://hfimfg.com\&sz=32)

HFI Manufacturing



[HFI restaurant equipment manufacturing](https://hfimfg.com/industries-we-serve/restaurant-equipment/?utm_source=chatgpt.com)

[Anderson Dahlen Inc. | ProFood World](https://images.openai.com/static-rsc-4/U8B77JFp9-JAKEHBKOgnNcduF6iHBmZsETT_VhoCXTZTdjSPA0nfAnAX5YMMOWaiBiIk0rMgyODEeUkJMDmYRoMYFuwf8mD8yzHUwbPT2gM1zEMRP1N05qqK2MNpo3GTZkO5nsnu8_YPltJmGM5sAM7USRBhvX9sO-bcrbmdRRM?purpose=inline)

**6. Anderson Dahlen**

Manufactures custom food-processing equipment, including mixing and blending systems, storage vessels, pump feeders, and batch-processing equipment. It could be approached for engineering review or US prototype construction.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://andersondahlen.com\&sz=32)

Anderson Dahlen



[Anderson Dahlen food processing](https://andersondahlen.com/markets/food/?utm_source=chatgpt.com)

**Manufacturing recommendation:** Request quotations from MBC, Longmai, and Chengchuan for the overseas prototype, while separately requesting an engineering and fabrication proposal from one US manufacturer. Compare the complete delivered cost, not just the factory's quoted equipment price.

The listed Chinese equipment prices found during research include approximately $5,800 for one MBC jacketed cooking-pot listing and substantially higher prices for larger industrial systems. These are prices for different existing machines, not quotations for this proposed custom appliance.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.sourcingai.com\&sz=32)

SourcingAI+2



## **11. Cost-control and manufacturing strategy**

The machine should be developed in three manufacturing stages.

| Stage   | Work                          | Objective                                                               |
| ------- | ----------------------------- | ----------------------------------------------------------------------- |
| Stage 1 | Engineering and CAD prototype | Validate dimensions, cartridge feeding, mixing, heating, and dispensing |
| Stage 2 | Functional prototype          | Test all five recipes, cleanability, controls, and food safety          |
| Stage 3 | Pilot manufacturing           | Build a small batch for restaurant testing before volume production     |

To reduce cost, use commercially available industrial components rather than asking the factory to manufacture every component from scratch.

For example:

- Purchase an established PLC rather than developing a proprietary controller.
- Use commercially available temperature sensors.
- Use standard industrial gear motors.
- Use an existing food-grade flow meter.
- Use standardized electrical enclosures and safety switches.
- Design the cartridge docking mechanism as a custom component, since it is central to the product.
- Use a standardized mixing vessel and heating assembly across all models.

The cartridge system, dosing mechanisms, recipe software, and dispensing assembly are the most important custom elements. These are where engineering resources should be concentrated.

A major cost-saving opportunity is to manufacture one central appliance that can prepare all five gravies, instead of developing five different machines.

## **12. Prototype acceptance requirements**

Before accepting a prototype, the purchaser should require the manufacturer to demonstrate the following:

| Test                  | Proposed acceptance target                                                   |
| --------------------- | ---------------------------------------------------------------------------- |
| Cartridge recognition | Correctly identifies each of five cartridges                                 |
| Water metering        | Within ±2% of programmed quantity, subject to validation                     |
| Ingredient dosing     | Within ±2% of validated recipe weight, subject to ingredient characteristics |
| Batch capacity        | Successfully prepares 1-, 2-, and 4-quart batches                            |
| Mixing                | No persistent dry pockets or unacceptable lumps                              |
| Heating               | Reaches and records the validated recipe conditions                          |
| Dispensing            | Transfers the batch without repeated blockage                                |
| Hot holding           | Maintains the approved holding temperature                                   |
| Cleaning              | Food-contact surfaces are accessible and cleanable                           |
| Fault protection      | Stops safely during sensor, motor, water, and heating faults                 |

The acceptance test should be witnessed or independently documented. The manufacturer should supply test records, photographs of internal assemblies, electrical diagrams, component certificates, and a list of replacement parts.

## **13. Intellectual property and manufacturing agreement**

Before sending detailed CAD files to overseas suppliers, have the business establish ownership and confidentiality terms.

The manufacturing agreement should state that:

- All custom drawings, cartridge designs, software, and product-specific engineering paid for by the purchaser belong to the purchaser.
- The supplier cannot sell the same proprietary cartridge interface or machine design to another customer without written permission.
- Production changes require written approval.
- The factory must disclose component substitutions.
- Quality inspections are permitted before shipment.
- Warranty, replacement parts, and service response times are specified.
- The factory must not use the purchaser's branding without authorization.

A nondisclosure agreement is useful, but it is not a substitute for a clear manufacturing and intellectual-property agreement. Have US and Chinese commercial counsel review the arrangement before transferring final production files.

## **14. Request for quotation to manufacturers**

The following is a preliminary manufacturing inquiry that can be sent to the companies listed above.

Dear Manufacturing and Engineering Team,

We are seeking a manufacturing partner to develop a custom commercial automated gravy preparation and dispensing machine for restaurant food-service operations.

The proposed machine will accept five replaceable dry-ingredient cartridges, with an expandable design supporting up to eight cartridges. Each cartridge will contain a standardized gravy formulation. The machine will connect to a potable-water supply, automatically meter water and ingredients, mix the formulation, heat and cook the gravy, and dispense the finished product into a removable heated serving pan.

The preliminary machine dimensions are approximately 30 inches wide, 32 inches deep, and 60 inches tall. The mixing vessel will have an approximate two-gallon capacity and will support finished batch sizes of one, two, and four quarts.

The required manufacturing scope includes:

1. Stainless-steel enclosure and structural frame.
2. Five-cartridge ingredient docking and identification system.
3. Motorized precision ingredient dosing mechanisms.
4. Metered potable-water inlet and filtration interface.
5. Stainless-steel mixing vessel and variable-speed agitator.
6. Electrically heated cooking chamber.
7. Automated temperature and process controls.
8. Sanitary gravy discharge valve.
9. Removable heated serving-pan compartment.
10. Industrial PLC and touchscreen control system.
11. Emergency stop and independent safety protections.
12. Cleaning and maintenance access.
13. Complete electrical and mechanical documentation.

We would like to receive information about your engineering and OEM/ODM capabilities, including whether your company can manufacture a custom compact machine rather than simply supply a larger industrial cooking kettle.

Please provide:

- An initial engineering and design estimate.
- Prototype manufacturing price.
- Estimated production cost at quantities of 10, 50, 100, and 500 units.
- Estimated manufacturing and delivery timelines.
- Available food-equipment and electrical certifications.
- Warranty and after-sales service arrangements.
- Whether you can provide 3D CAD drawings, electrical schematics, PLC programming, and a complete bill of materials.
- Whether you can manufacture the proprietary ingredient cartridge assembly.
- Whether you can support testing with five different gravy formulations.

We are interested in establishing a long-term manufacturing relationship, beginning with one fully functional prototype and progressing to a pilot production order if the machine meets its performance and certification requirements.

Please identify the engineering information you require to prepare a formal quotation.

Sincerely,

Product Development and Equipment Procurement Team

## **15. Immediate construction roadmap**

The next practical step is to commission a mechanical and electrical engineering package rather than immediately ordering a production machine.

1. **Finalize the recipe and cartridge specifications.**

   Determine the dry ingredient weight, water ratio, cartridge volume, and expected output for each of the five gravies. This information controls the size of the feeders and mixing vessel.
2. **Complete the engineering drawings.**

   Prepare 3D CAD models, component dimensions, wiring diagrams, piping layouts, and manufacturing tolerances.
3. **Obtain three Chinese factory quotations and one US quotation.**

   Require each supplier to quote the same specifications so that their offers can be compared fairly.
4. **Build one complete prototype.**

   Test it with actual gravy formulations, not just water or thin sauce.
5. **Complete independent food-safety and electrical evaluation.**

   Address applicable sanitation standards, electrical certification, cleaning validation, and food-code requirements before restaurant installation.
6. **Run a restaurant pilot.**

   Test production speed, cartridge replacement, employee usability, gravy consistency, waste, and maintenance before approving a production run.

**My recommendation:** Develop the first prototype with a Chinese OEM factory that already builds jacketed sauce cookers, but retain control of the cartridge design, recipe software, and engineering drawings. Have the completed prototype independently evaluated in the United States before ordering multiple units. This offers a path to lower manufacturing costs without compromising food safety, reliability, or ownership of the product design.
