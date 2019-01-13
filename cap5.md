# Cap 5 - Manufactoring Integration

Includes planning and execution of the materials and manufacturing functions, plus the supply network that feeds those activities.

It also includes quality and maintenance, because they are integral to the manufacturing and materials process.

### Discussed functions:

- Material and Capacity Planning
- Manufacturing Execution Systems (Enterprise Production Systems).
- Just-In-Time (JIT)
- Advanced Planning and Scheduling
- Supplier Integration
- Quality Management Systems
- Maintenance

## Material and Capacity Planning _(slide 2)_

Material and capacity planning includes the following functions:

- Master Production Scheduling (MPS).
- Rough-Cut Planning the capacity side of master production scheduling.
- Material Requirements Planning (MRP), the original foundaton of MRP 2 systems.
- Capacity Requirements Planning (CRP), the capacity reporting system that corresponds to MRP.
- The perpetual inventory system.

### Master Production Schedule (MPS) _(slide 3)_

The Master Scheduler has the final answer to the question, "When can we ship an order to Customer X?"

- A Master Production Scheduler, or Master Scheduler, continually balances demand and production by monitoring fluctuations in actual customer demand and/or forecasts actual production and supply, and adjusting the production schedule, using inventory as a buffer.

**Virtually all manufacturers run their Master Production Scheduling programs at least weekly, many run them daily, and some even run them continuosly.**

#### Integration _(slide 3)_

The Master Schedule must be integrated with the following systems to receive accurate input:

- Demand
- Material Supply
- Capacity Supply

#### System Wich Feed MPS, functions affected by MPS

Veja slide 4.

### Rough Cut Planning _(slide 4)_

Rough-Cut Resource Planning explodes the master schedule, using rough-cut routings, to determine the approximate load on each critical resource during each user-specified time period.

Any resource loads that exceed capacity, or maximum, are flagged for review by the Master Scheduler.

#### Integration _(slide 5)_

From a technical standpoint, Rough-Cut Planning (RCP) directly integrates only with the Master Production Schedule.

However, management should define all business contrains that it wants RCP to check, including:

- Capacity, internal.
- Capacity at suppliers.
- Transportation.
- Cash.
- Labor.
- Skilled Setup.
- Machine operators.
- Warehouse space.
- Energy (if on an interruptible service contract).
- Materials.

### Material Requirements Planning (MRP) _(slide 5)_

It views the world like an expeditor, trying to predict all futures shortages, then work around them by ensuring that the parts arrive just when needed.

_Except for TEI systems that use APS as the planning engine, MRP is the central planning module for all MRP, MRP 2, ERP, and some TEI systems_

#### MRP Major inputs _(slide 5)_

- The Master Production Schedule, for demand.
- Inventory status.
- Schedule Receipts (open orders) from shop floor and from suppliers.
- The Bill of Materials.

#### MRP Two Major Outputs _(slide 6)_

- Full MRP report
  - which projects on the on-hand inventory status of each item to the end of the planning horizon (at least 6 months, and sometimes a year into the future).
- MRP Action Report

  - which contains the exceptions that materials planners must take action on, including rescheduling existing orders (both manufactured and purchased) and releasing new orders (both manufactured and purchased).

#### Integration _(slide 6)_

MRP is still the detailed planning heart of most ERP and many TEI systems.

It uses information from MPS and many of the same areas as MPS, including the ones in **image (slide 6)**.

### Capacity Requirements Planning (CRP)

One of MRP's major weakness is that is assumes infinite capacity, both inside the company and at suppliers.

In companies where the assumption is unrealistic, the CRP report is critical to successful operation, because it predicts which resources will have capacity problems so that planners can take action.

#### When CRP predicts capacity problems: _(slide 7)_

Material planners and/or the master scheduler must take corrective action. If the problem is too little capacity, the corrective options include:

- Using alternate machines or work centers.
- Using substitute parts or assemblies.
- Outsourcing one or more work orders.
- Working overtime (short term), adding a shift (long term).
- Acquiring (buying or leasing) more equipment.
- Delaying the final customer shipment or back ordering.

**Before the advent of executive decision support tools, decision makers had great difficulty predicting the actual impact of their capacity decisions on the company's profit and loss.**

If the problem is too much capacity, the corrective include:

- Shipping orders to customers early.
- Encouraging the sales force to sell more.
- Subcontracting our excess capacity.
- Cutting hours for the work force, temporarily (enforcing vacations).
- Layoffs.

#### Integration _(slide 7)_

Because of the detailed nature of its calculations and reports, CRP requires detailed data about the state of completion of each scheduled receipt in the shop.

**CRP is merely a report**

Planners and management **use this report to make decisions** that can affect many functions and departments.

### Inventory _(slide 8)_

Whenever material moves between the stockroom and the plant floor, or through a critical work center, cell, or line, the TEI system needs to be informed so that it can accurately report the current location of each item.

A perpetual inventory system needs to have the ability to be adjusted:

- by cycle counting (using the APICS two-step process)
- by an annual physical inventory.

Many TEI systems can track material usage.

#### Inventory Inputs _(slide 8)_

Veja imagem do slide.

#### Conclusion _(slide 8)_

- Since on-hand inventory balances are the starting point for MPS and MRP planning and for customer order promising, they must be absolutely accurate.
- Therefore, most inventory systems support cycle counting.

## Manufacturing Execution Systems (Enterprise Production Systems) _(slide 9)_

Shop fllor systems were communicating MRP's detailed requirements to the shop floor in the 1970's, with dispatch lists and priority lists.

However, there was a significant gap between the planning systems and actual execution, because the planning data was frequently late and was rarely current or sufficiently accurate.

Many systems evolved to integrate execution to planning, including data collection work-order-tracking and SPC.

### A Manufacturing Execution System (MES) _(slide 9)_

Is a on-line, integrated, computerized system that is the accumulation of methods and tools used to accomplish production.

Real-time MES systems respond to minute-to-minute changes on plant floor. ERP and TEI systems tend to repond daily.

An MES is the best way to manage environments that require work orders on a shop floor (and therefore are not suited for kaban or visual flow techniques).

### Manufacturing Execution Systems _(slide 9)_

Are intended to hekp manufacturing management, from top management to the shop floor, manke decisions that coordinate production most effectively.

An MES is more than a planning tool (contrasted with MRP, which is only a planning tool).

**MES is an on-line extension of MRP that emphasizes execution, including:**

- Making products
- Turning machines on and off.
- Measuring parts.
- Changing order priorities.
- Setting and reading controls that measure...

### MES & ERP

#### MES Functionality

Two categories: core functions and support functions.

##### Core functions include: _(slide 11)_

- **Planning system interface**, which provides MES integration with...
- **Work order and PLC management**, which manages and schedules work throughout the plant using a real-time view, including...
- **Workstation (work center and machine) management**, which implements the work order plan at the work station, and plans and schedules each operational work station, including...
- **Inventory tracking and management**, which develops, stores, and maintains the details of each lot of unit aof inventory. For the purposes...
- **Material movement management**, which determines and causes materials to be moved from their current location to their needed location at the right time...
- **Data collections acts as a clearinghouse** and translator for all information that is generated within the plant, thereby allowing the MES to remain current. The different kind of physical sources...

There is a three-tier leve of systems applicable to manufacturing

- TEI: decision suppport systems.
- MES and control levels system such as PLCs: on-line transaction processing systems.

### Enterprise Production Systems _(slide 12)_

Are the integration of MES,plant floor applications and controls.

Integrating all real-time activities into one system can result in much simpler hardware configurations, and real-time information availability that is more responsive to plant events as they occur.

## Just-In-Time (JIT) _(slide 12)_

Is a "pull" system, meaning that no materials move and no work is done until a downstream customer consumes a product.

JIT is much more than a scheduling system, it is also a philosophy that focuses on identifying and eliminating all waste, and on continuos improvement.

HIT identifies seven wastes:

- Overproduction, Waiting, Transportation, Processing Stock( inventory), Motion, Making defective products.

## Advanced Planning and Scheduling _(slide 13)_

Capitalizing on the availability of very powerfull and very inexpensive computer technology.

- APS (Advanced planning and Schedulling) systems use linear programming and other advanced mathematics to optimize schedules at varying levels in an organization.

- The simplest level is the local plant, in which the APS maximizes management's choice of one or more metrics, including on-time customer deliveries, profits, and labor force stability.

### Purchasing _(slide 14)_

Purchasing is integral to achieving on-time shipments at profitable margins.

In many manufacturers, purchased items accounts for more than 50% of the cost of goods sold; in those companies, a 5% saving in purchased items results in a 2.5% increase in profit before taxes.

### Supplier Integration _(slide 14)_

Types of Integration:

- Manual integration, Electronic, Fully Integrated, Other Methods...

## Quality Management Systems and Maintance Management System

Ver slide 15.
