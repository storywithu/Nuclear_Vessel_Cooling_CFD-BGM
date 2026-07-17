# Project: Nuclear Reactor Cooling System Thermal-Hydraulic Analysis

### A. System Geometry & Boundary Conditions ### 
#### Geometry & Specifications
| Specification | Value | Note |
| :--- | :--- | :--- |
| **Internal Vessel Volume** | 0.1113 m³ | Effective coolant capacity |
| **Vessel Internal Diameter** | 0.4 m | Main cylindrical body diameter |
| **Vessel Total Length** | 1.0 m | Total longitudinal flow path |
| **Fuel Rod Bundle** | 25 ea | Core heating element configuration |
| **Shroud Diameter** | 0.3 m | Flow channel optimization for heat transfer |
| **Inlet Velocity** | 1.0 m/s | Regulated coolant mass flow rate |
| **Inlet Temperature** | 19.85 ℃ | Initial coolant operational temperature |
| **Wall Temperature** | 90.0 ℃ | Simulated thermal load from fuel rods |
| **Outlet Pressure** | 0 bar | Ambient discharge condition |

![Geometry]

<img width="915" height="652" alt="image" src="https://github.com/user-attachments/assets/5bda56cc-bfe1-4948-9bc4-0593e4630845" />
<img width="862" height="718" alt="image" src="https://github.com/user-attachments/assets/0f54ff30-bec8-46d3-8959-0013315c3951" />
<img width="948" height="703" alt="image" src="https://github.com/user-attachments/assets/22adef9d-b48d-416f-b8d5-8e6cdcfbc3bf" />

### B. Mesh Configuration & Quality ### 
- **Total Cell Count**: Approx. 5.53M cells
- **Quality Metrics**: The mesh shows excellent consistency with average Aspect Ratio and Skewness values well within the acceptable industrial standards, ensuring high numerical stability.
  
![Mesh]
<img width="887" height="527" alt="image" src="https://github.com/user-attachments/assets/72cecf62-18a8-41da-85d2-d2d02cacc259" />
<img width="659" height="782" alt="image" src="https://github.com/user-attachments/assets/21242b85-9890-4f9c-a220-24d93bec7c81" />

### C. Flow Dynamics Result ### 
**- Result**:  

<img width="1000" height="500" alt="2" src="https://github.com/user-attachments/assets/c01192eb-326a-480d-9f8e-214ae080452c" />

**- Residuals Plot**: Confirmed convergence of the governing equations.
<img width="1589" height="822" alt="image" src="https://github.com/user-attachments/assets/5c250b87-04ea-4063-976a-798636e16988" />

## 1. Executive Summary
- **Objective**: (무엇을 해결하려 했는가? 예: 원자로 노심의 효율적인 열 제거 성능 평가)
- **Key Outcome**: (결과물은 무엇인가? 예: 냉각재 유동 분포 가시화 및 핫스팟 제거 확인)
- **Methodology**: (사용 툴 및 핵심 물리 모델)

- | Parameter | Simulation Setting |
| :--- | :--- |
| **Turbulence Model** | k-omega SST |
| **Algorithm** | SIMPLE |

## 2. Technical Specifications & Modeling Assumptions
### Geometry & Domain
- (치수 대신 개념 기술): The model focuses on the pitch-to-diameter ratio of the fuel bundle to optimize coolant flow path and minimize pressure drop.

### Boundary Conditions
- **Inlet**: (값 입력) - (이유: 실제 작동 조건 모사)
- **Outlet**: (값 입력) - (이유: 대기압 조건 등)
- **Walls**: (핵심 내용): No-slip and constant heat flux conditions applied to fuel rod surfaces to resolve thermal boundary layer and convective heat transfer coefficient.

## 3. Mesh & Quality Assurance
- **Mesh Statistics**: (Total Cells / Element Types)
- **Quality Status**: Passed (SimScale criteria verified for structural and numerical stability)

## 4. Results & Engineering Insights
- **Flow Visualization**: (결과 해석: 유속이 균일한가? 특정 구간에서 정체되는가?)
- **Thermal Performance**: (온도 분포: 예상했던 최고 온도 지점과 해석 결과 비교)

 <img width="600" height="687" alt="image" src="https://github.com/user-attachments/assets/1a447801-4695-48cc-b418-e063bc56898d" />


## 5. Critical Reflection & Future Advancement
- **Modeling Limitation**: (왜 이 가정을 했는가? 예: Steady-state vs Transient)
- **Future Advancement**: (더 발전시킨다면? 예: 시간 의존적 해석(Transient)으로 연료봉의 열팽창까지 고려)
