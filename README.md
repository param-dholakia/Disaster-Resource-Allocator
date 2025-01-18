# Disaster-Resource-Allocator
Disaster Resource Allocator is a Java-based project that calculates risk scores for districts based on population, land type, and urbanization to optimize resource allocation during disasters. It ensures efficient distribution by prioritizing high-risk areas with limited resources.


# Risk-Based Resource Distribution

A Java-based application that calculates risk scores for districts and optimizes resource allocation during disasters. The system evaluates each district's population, land type, urbanization, and resource demand to prioritize high-risk areas for effective disaster response.

---

## Features
- **Risk Assessment**: Calculates a risk score for each district based on population, land type, and urbanization.
- **Resource Allocation**: Distributes available resources efficiently, prioritizing districts with higher risk scores.
- **Dynamic Sorting**: Uses risk-to-demand ratio for optimal allocation.
- **Partial Allocation Support**: Handles scenarios where resource demands exceed availability.

---

## How It Works
1. Input district details: Name, population, land type, urbanization, and resource demand.
2. Risk scores are computed using weighted factors.
3. Districts are sorted based on their risk-to-demand ratio.
4. Resources are allocated starting with the highest priority district.
5. Unused resources (if any) are reported.

---

## Project Structure
- **RiskStatistics.java**: Contains methods for calculating risk factors based on population, land type, and urbanization.
- **District.java**: Defines the `District` class with attributes and methods for handling district information.
- **DisasterResponse.java**: Main driver class for input handling, risk computation, and resource allocation.

---

## Input Details
1. **Number of Districts**: Specify the total number of districts.
2. **Total Resources**: Enter the total resources available for allocation.
3. **District Data**:
   - Name
   - Population
   - Land Type: Choose from Forest, Coastal, Desert, or Urban.
   - Urbanization: Choose from Rural, Suburban, or Urban.
   - Resource Demand

---

## Output
- Displays the risk scores of all districts.
- Allocates resources to districts based on priority.
- Reports remaining resources or marks incomplete allocations.

---

## How to Run
1. Compile the project:
   ```bash
   javac DisasterResponse.java
2. Run the Program
   ```bash
   java DisasterResponse
3. Example Output
```
Enter the number of districts: 3
Enter the total available resources: 100

Enter details for District 1:
Name: Alpha
Population: 20000
Available Land Types: 
1) Forest  2) Coastal  3) Desert  4) Urban
Enter choice: 4
Available Urbanization types: 
1) Rural  2) Suburban  3) Urban
Enter choice: 3
Enter Resource demand for Alpha: 50
--------------------------------

Enter details for District 2:
Name: Beta
Population: 5000
Available Land Types: 
1) Forest  2) Coastal  3) Desert  4) Urban
Enter choice: 1
Available Urbanization types: 
1) Rural  2) Suburban  3) Urban
Enter choice: 1
Enter Resource demand for Beta: 30
--------------------------------

Enter details for District 3:
Name: Gamma
Population: 60000
Available Land Types: 
1) Forest  2) Coastal  3) Desert  4) Urban
Enter choice: 2
Available Urbanization types: 
1) Rural  2) Suburban  3) Urban
Enter choice: 2
Enter Resource demand for Gamma: 40
--------------------------------

Risk Score of Alpha : 24
Risk Score of Beta : 8
Risk Score of Gamma : 19

Resource Allocation...
Allocating 50 resources to Alpha
Allocating 30 resources to Gamma
Allocating 20 resources to Beta (partial allocation)

All resources have been allocated.
```
## 5. Technologies Used
   Java: Core language used for implementation.
  Scanner: For user input handling.
  Arrays: For storing and sorting district data.
