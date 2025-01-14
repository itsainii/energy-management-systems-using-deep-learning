# Energy-Management-Systems-Using-Deep-Learning

**1. Introduction**

The increasing adoption of microgrids with renewable energy systems, driven by environmental and socioeconomic factors, faces challenges such as renewable energy variability and dynamic load fluctuations, leading to increased grid consumption. This study addresses these challenges by proposing an advanced Energy Management System (EMS) integrated with a Deep Learning model for load forecasting. The objective is to enhance the efficiency and cost- effectiveness of microgrids by dynamically adjusting to forecasted load demands. The EMS utilizes Long Short-Term Memory (LSTM) networks to predict the load demand of a commercial building, allowing for optimized battery scheduling and reduced reliance on the utility grid. The study conducted a month-long simulation using real historical load and solar power data, comparing the proposed EMS with a standard EMS. Key findings indicate that the proposed EMS significantly reduces grid consumption, resulting in a 9.3% reduction in monthly electricity bills. Integrating deep learning in EMS demonstrates substantial improvements in handling dynamic conditions and optimizing energy usage. These findings imply that deep learning-based EMS can lead to significant cost savings and more efficient microgrid energy management, promoting the broader adoption of renewable energy solutions.

**2. Objectives**
1. To develop load forecasting of commercial building using deep learning model.
2. To implement an energy management system microgrid integrated with deep
learning load forecasting.
3. To evaluate the performance of proposed energy management system by comparing
the electricity bill with standard energy management system.

**3. Methodology**

3.1 Proposed Microgrid Design

The microgrid's proposed block diagram is shown below. The PV panel generates power from sunlight, stored in the
Battery Energy Storage System (BESS). The BESS acts as the
main supplier, providing power to the load. The utility grid
supplies the remaining power if the power stored in the BESS
does not fulfill the load demand. A Deep Learning Energy
Management System (DL EMS) is integrated to analyze
current power conditions and forecast load demand, deciding
optimal strategies for charging and discharging the battery in
the microgrid, thereby reducing power consumption from the
utility grid.

<img width="368" alt="Screenshot 2025-01-14 at 7 22 03 PM" src="https://github.com/user-attachments/assets/5af680f6-431d-48f0-b022-72ddf576bac3" />


3.2 Proposed EMS Algorithms

Two algorithms proposed are EMS strategies and EMS
with Load Forecasting algorithms. Figure below is EMS strategies to ensure that load demand is fulfilled which also abides SOC battery constraints. It determines whether to charge or discharge the battery or to supply power from the grid to the load. to avoid overcharge and over-discharge.

<img width="387" alt="Screenshot 2025-01-14 at 7 23 49 PM" src="https://github.com/user-attachments/assets/1ca31eab-45ad-4099-a5d6-1e09a74af8f7" />

3.3 Proposed EMS Algorithm with LSTM Load forecasting

Fig. below illustrates the proposed EMS integrating load
forecasting. The system collects daily load forecasts and
identifies the time of the highest predicted load. During peak
periods, it prioritizes charging the battery before the next
expected peak period. This approach ensures sufficient battery
power to meet the load demand during peak times. The EMS
also considers battery SOC constraints, charging the battery if
the SOC is below SOCmax or discharging if it exceeds SOCmin
, and stops charging when SOC reaches SOCmax.

<img width="364" alt="Screenshot 2025-01-14 at 7 23 58 PM" src="https://github.com/user-attachments/assets/a64903f2-9b1c-4900-a3bf-ea883aad3e45" />


**4. Result**

Fig. below illustrates the comparison between the total costs of the
proposed EMS and the standard EMS. The red circles
highlight the days when the total cost of the proposed EMS
exceeds that of the standard EMS. There is a total of 9 days
where the proposed EMS incurs higher costs than the standard
EMS. However, this result is acceptable because there are
more days where the proposed EMS's costs are significantly
lower, leading to overall savings.


<img width="513" alt="Screenshot 2025-01-14 at 7 25 25 PM" src="https://github.com/user-attachments/assets/fa0c5bd8-c377-46be-bc39-93310854b7de" />

Figure below shows the daily costs for the proposed EMS and
the standard EMS during peak and non-peak hours over a
month. During non-peak hours, the costs are identical for both
EMS because both systems prioritize battery charging during
these times due to the lower electricity prices. However,
during peak hours, the proposed EMS incurs significantly
lower costs than the standard EMS, with a difference of
RM12,679.88. Overall, the total monthly cost is calculated for
both systems, demonstrating that the proposed EMS achieves
**a 9.23% reduction in total costs** compared to the standard
EMS.

<img width="378" alt="Screenshot 2025-01-14 at 7 25 30 PM" src="https://github.com/user-attachments/assets/f3e7d3db-d6cf-4f50-84e9-17dc75c506ba" />


