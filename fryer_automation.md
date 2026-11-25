# Frying Solution: Full-Task Handling, Grease Management, and Service Station Delivery System

## Executive Summary

This solution designs an **integrated frying and oil management subsystem** as a component of the Bojangles restaurant automation plan. The system must accomplish four core tasks: batch frying products (chicken, country fried steak), oil filtration and purification, waste oil discharge and recycling interface, and delivery of finished products to the service station. The design principle is **modular integration**—combining the frying host, filtration loop, oil storage tank group, and delivery mechanism into a single coordinated unit rather than a simple patchwork of dispersed equipment. For manufacturer selection, **Henny Penny** has the most direct relevance for fried chicken applications (pressure fryers and oil management); **Frymaster** and **Pitco** offer highly reliable open fryers and mature filtration systems; the oil recycling end is served by **DAR PRO Solutions** or **Restaurant Technologies**, which provide nationwide waste oil collection and equipment interface services. The cost-effectiveness logic of this solution lies in converting oil management from a cost center into a quantifiable source of savings by extending frying oil life, reducing manual filtration labor, and eliminating the safety risks of waste oil handling.

---

## Part One: System Architecture—Integration of Four Functional Modules

### 1.1 Frying Host Module

The frying host is the core of the system, responsible for batch frying chicken and country fried steak. Bojangles' fried chicken process is characterized by hand-breading and open frying, so host selection should prioritize **open fryers** over pressure fryers unless the brand decides to adopt pressure frying for specific product lines. Henny Penny's pressure fryers have advantages in fried chicken operations, offering programmable controls, dedicated cooking programs, and oil management features, but pressure fryers require approved recipes, specific loading procedures, and safety training—they are not a direct substitute for standard open fryers. For Bojangles' existing product system, the flexibility of open fryers is higher, compatible with fried chicken, fried steak, and potential future limited-time products.

Host capacity specifications should be determined based on the actual output requirements during peak hours at individual stores. Using the Henny Penny Ultra-Fry series as a reference, the Ultra-Fry 20 can process approximately 90 pounds of product per hour, and the Ultra-Fry 30 approximately 110 pounds per hour. If the peak half-hour window demand for a single store is 135 pounds, a single Ultra-Fry 30 would operate at 122% load, causing accelerated oil degradation, uneven browning, and premature motor drive wear. Therefore, capacity calculation should be based on **peak half-hour demand plus 20% buffer**, not average hourly output. For most Bojangles stores, a dual Ultra-Fry 20 configuration is superior to a single Ultra-Fry 30 in both redundancy and total cost.

### 1.2 Filtration and Purification Loop

The filtration loop is the key link in oil management, with the function of automatically removing food particles, flour residue, and polar compounds from the oil during frying or between batches. Henny Penny's ThermoGuard filtration system and automatic skimming cycle have been validated by third-party laboratories to reduce free fatty acid (FFA) accumulation by 47% compared to manual skimming, thereby extending oil change intervals by 12% to 18% and saving $1,100 to $1,800 annually in oil and disposal costs. This data has cumulative effects at Bojangles' scale: if all 800+ stores in the system deploy similar filtration capabilities, annual savings could reach millions of dollars.

The engineering implementation of the filtration loop references mature designs from commercial fryer patents. Patent literature describes an oil processing architecture for dual-fryer systems: the controller coordinates the path of oil from fryer to filter tank and back to fryer through selector valves, filter pumps, and storage pumps, with check valves preventing oil backflow. Core components of this architecture include: drain valves (independently controlled per fryer), filter pumps, storage pumps, selector valves, temperature sensors, and controllers. The controller's processor receives temperature sensor signals and drives...

Pitco's Solstice Supreme series, as used by Zaxby's, provides a reference configuration: dual full-size frypots with under-fryer filtration, rear oil return, and an 8 GPM filter pump for circulating filtered oil back to the frypots. This under-fryer filtration design reduces direct oil handling and streamlines routine filtration. Pitco's enhanced ROV (Reduced Oil Volume) fryers feature a filter cycle that completes in approximately 3.5 minutes, with dual oil return jets replacing the old single-jet design to clear sediment faster and reduce clogging. These specifications are critical for Bojangles because filtration speed directly determines whether employees will actually perform filtration during peak periods—slow filtration cycles are often bypassed, accelerating oil degradation.

Henny Penny's Smart Touch Filtration™ allows filtration of one vat while continuing to cook in others, with Oil Guardian® automatically topping off oil levels based on sensor readings. This "filter while cooking" capability is essential for high-volume QSR environments, where stopping all frying for filtration is operationally unacceptable. Frymaster's FilterQuick 30 electric fryer offers comparable capability: 30-pound oil capacity, automatic filtration, automatic top-off (ATO) from a Jug-in-Box (JIB), and an optional Oil Quality Sensor (OQS) for real-time oil health monitoring. The Frymaster approach uses 40% less oil than traditional 50-pound models while using 10% less energy.

### 1.3 Waste Oil Discharge and Recycling Interface

Waste oil management is where safety and compliance intersect. Manual draining of hot oil creates serious burn risks and contamination issues, and may incur fines for improper disposal. The system should include an **automatic oil disposal system** that safely routes used oil to storage or disposal tanks, removing human contact from the process. Pitco's Smart Solstice line includes this as an integrated feature.

For the recycling end, two service models are available. **DAR PRO Solutions** connects directly to fryers for quick, effortless used cooking oil (UCO) draining at the touch of a button, with seamless piped connections discreetly installed behind walls or in ceilings. Their trained experts collect UCO via secure external connections, enabling 24/7 service without kitchen disruption. DAR PRO's DarLinQ™ platform provides real-time oil-level monitoring, route optimization, and theft deterrence, backed by 90+ facilities and 2,100+ trucks covering over 90% of the U.S. population.

**Restaurant Technologies** offers a fully managed Total Oil Management model: automated oil delivery (bulk fresh oil delivered on schedule directly to the tank), hands-free disposal (used oil pumped out without lifting, burns, or mess), and used oil recycled into biofuel. They install everything at no upfront cost, and most kitchens find the service pays for itself through labor and oil savings. They service nationwide with 41 depots covering all metropolitan markets and work with the vast majority of commercial fryer models used in QSR. For Bojangles, the managed service model offloads equipment maintenance, oil procurement, and waste coordination, which is attractive for franchisees who lack the bandwidth to manage these functions independently.

### 1.4 Delivery to Service Station

The finished product delivery mechanism connects the frying host to the front-line service station. For Bojangles' operation, the most practical approach is a **heated holding and transfer cart** or a **conveyor-based delivery system** depending on store layout. The frying host deposits finished product into a heated transfer container (maintained at 150°F to 160°F), which is then moved to the service line by a staff member or an automated guided vehicle (AGV) in higher-volume stores. The transfer container should be vented to allow steam escape, consistent with the packaging principles described in earlier volumes—sealed containers trap moisture and degrade crust crispness.

For stores with the underground or back-of-line transfer infrastructure described in the broader automation blueprint, the frying host can discharge directly into an insulated conduit that delivers product to a holding unit behind the service counter. This eliminates the manual transfer step and reduces the window during which product sits unprotected. The delivery mechanism should be integrated with the holding-time management system: when product enters the transfer conduit, a timer starts, and the service-line holding unit displays the remaining hold window.

---

## Part Two: Manufacturer Capability Matrix and Selection Rationale

| Manufacturer | Core Strength | Relevant Products | Fit with Bojangles Automation Plan |
|-------------|--------------|-------------------|-----------------------------------|
| **Henny Penny** | Fried chicken specialization; oil volume reduction; integrated filtration | Evolution Elite (40% less oil), Smart Touch Filtration, Oil Guardian automatic top-off | Highest fit for fried chicken; pressure fryer option if recipe approved; strong oil savings story |
| **Frymaster** | Electric fryer efficiency; automatic filtration; oil quality sensing | FilterQuick 30 (30-lb capacity, ATO, built-in filtration, OQS) | Strong for electric-only stores; oil quality sensor provides data integration point |
| **Pitco** | High-volume gas frying; under-fryer filtration; automatic disposal | Solstice Supreme (used by Zaxby's), ROV series (3.5-min filter cycle, 8 GPM pump) | Proven in chicken QSR; fast filtration encourages compliance; automatic oil disposal feature |
| **DAR PRO Solutions** | Waste oil collection and recycling; direct fryer connection | Piped UCO draining, DarLinQ monitoring, 24/7 external collection | Handles the recycling end; reduces manual handling and compliance risk |
| **Restaurant Technologies** | Fully managed oil lifecycle (delivery, filtration, disposal) | Total Oil Management (no upfront equipment cost, bulk delivery, hands-free disposal) | Best for franchisees seeking turnkey solution; nationwide coverage |

The selection logic is not to choose a single manufacturer for everything but to **combine the best-fit components**. Henny Penny or Pitco for the frying host and filtration; DAR PRO or Restaurant Technologies for waste oil interface. The equipment should be specified with **oil reclamation connection points from the factory**—as noted in industry guidance, these parts are not very costly when installed at the factory but can be expensive to add later.

---

## Part Three: Cost-Effectiveness Analysis

### 3.1 Oil Savings

The most significant operating cost in frying is oil, not equipment. Henny Penny's Evolution Elite uses 40% less oil per vat, and Frymaster's FilterQuick 30 uses 40% less oil than traditional 50-pound models. For a Bojangles store using 100 pounds of oil per week, a 40% reduction saves 40 pounds per week, or approximately 2,080 pounds per year. At a bulk oil cost of $1.50 to $2.00 per pound, annual savings are $3,120 to $4,160 per store. Across 800 stores, this is $2.5 million to $3.3 million annually.

### 3.2 Filtration-Driven Oil Life Extension

Better filtration extends oil life by removing the particles that accelerate degradation. Henny Penny's data shows 12% to 18% longer oil life with its filtration system. If a store changes oil every 14 days without advanced filtration, a 15% extension adds approximately 2 days to each cycle, reducing annual oil changes from 26 to 22—a 15% reduction in oil purchases and disposal costs. Combined with the volume reduction, the total oil-related savings can reach 45% to 50% of baseline oil spend.

### 3.3 Labor and Safety Savings

Automatic filtration and automatic top-off eliminate the manual labor of checking oil levels, draining and filtering oil, and refilling. Pitco estimates that operators can lose thousands of dollars each year simply by neglecting daily filtration. The automated system enforces filtration at preset intervals without requiring employee memory or discipline. The automatic oil disposal system removes the burn risk from hot oil handling—one of the most common kitchen injuries—which can reduce workers' compensation costs and insurance premiums. Restaurant Technologies notes that "your insurer takes notice" when hands-free disposal removes the risk entirely.

### 3.4 Payback Estimate

For a single store, the incremental cost of an automated filtration and oil management system over a standard fryer is approximately $3,000 to $6,000, depending on the manufacturer and configuration. The annual savings from oil reduction, extended oil life, labor reduction, and safety improvement are estimated at $4,000 to $7,000. The payback period is therefore **12 to 18 months**, with continued savings thereafter. For franchisees using a managed service model (Restaurant Technologies), there is no upfront equipment cost, and the service fee is offset by the oil and labor savings from day one.

---

## Part Four: Integration with the Broader Bojangles Automation Plan

The frying solution is not a standalone system. It interfaces with three other systems described in this book series. First, the **holding-time management system**: finished product enters the transfer mechanism with a timestamp, and the service-line holding unit enforces the hold window. Second, the **data platform**: the fryer's controller (Henny Penny Smart Touch, Frymaster easyTouch, or Pitco Solstice controls) can export oil quality data, filtration cycle counts, and energy consumption to the Bojangles cloud dashboard, enabling corporate engineering to compare oil performance across stores and identify outliers. Third, the **automated side preparation system**: the fryer's oil management and the side modules' heating systems share the same electrical infrastructure and the same maintenance schedule, simplifying service coordination.

The Main Ingredient Test applies: does this frying solution make the chicken more flavorful, the crust more consistent, or the operation more affordable? The integrated filtration keeps oil cleaner, which means the breading absorbs fewer off-flavors and the crust stays golden rather than darkening prematurely. The automatic top-off maintains the oil level at the correct ratio to the food load, which means the chicken fries evenly rather than sitting in too little oil and becoming greasy. The automatic disposal removes the human error and safety risk from waste oil handling, which means the kitchen runs cleaner and the employee who would have been carrying a hot oil container is instead available to serve customers. Each element passes the test. Each element belongs.

---

**Appendix: Component and Cost Summary (Per Store)**

| Component | Function | Estimated Cost |
|-----------|----------|----------------|
| Frying host (dual vat, open fryer with automatic filtration) | Batch frying chicken and steak | $12,000–$18,000 |
| Oil Guardian / ATO system | Automatic oil level maintenance | Included in host or $1,500 add-on |
| Under-fryer filtration with 8 GPM pump | Fast filtration during service | Included in host |
| Waste oil discharge pump and connection | Hands-free disposal to recycling tank | $800–$1,200 |
| External waste oil tank (if not provided by recycler) | Storage for collection | $500–$1,000 or provided by DAR PRO/RTI |
| Heated transfer cart or conduit connection | Delivery to service station | $1,500–$3,000 |
| **Total incremental cost (over standard fryer)** | | **$3,000–$6,000** |
| **Estimated annual savings (oil, labor, safety)** | | **$4,000–$7,000** |
| **Payback period** | | **12–18 months** |
