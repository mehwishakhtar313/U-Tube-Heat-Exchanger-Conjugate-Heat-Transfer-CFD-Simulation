# U-Tube Heat Exchanger CFD Simulation — Conjugate Heat Transfer

## 1. Project Overview

This project investigates fluid flow and heat transfer in a U-tube heat exchanger using Computational Fluid Dynamics (CFD) in SimScale.

A conjugate heat transfer (CHT) simulation was performed to investigate temperature distribution and flow behavior in the shell-side and tube-side passages. The model uses water as the working fluid and steel as the solid material, with the **k–ω SST turbulence model** selected for turbulence modeling.

The workflow includes geometry preparation, fluid-region creation, imprinting, material assignment, boundary-condition specification, mesh generation, simulation execution, and post-processing.

## 2. Project Objectives

- Investigate temperature distribution within a U-tube heat exchanger.
- Analyze flow behavior in the shell-side and tube-side passages.
- Model thermal interaction between fluid regions and solid heat-exchanger walls.
- Generate a computational mesh for CFD analysis.
- Visualize temperature and velocity contours.
- Examine solver residuals and assess numerical convergence.
- Develop practical skills in CFD modeling and thermal analysis of process equipment.

## 3. Software and Simulation Setup

## Simulation Setup

| Parameter | Value |
| **Software** | SimScale |
| **Equipment** | U-tube heat exchanger |
| **Analysis Type** | Conjugate Heat Transfer (CHT) |
| **Turbulence Model** | k–ω SST |
| **Intended Analysis Approach** | Steady-state |
| **Working Fluid** | Water |
| **Solid Material** | Steel |
| **Fluid Regions** | Shell-side and tube-side |
| **Simulation End Time** | 1,000 s |
| **Geometry Preparation** | Flow-volume extraction and imprint |
| **Mesh Generation** | SimScale meshing workflow |

## 4. Geometry Preparation

The model represents a U-tube heat exchanger containing a shell, tube bundle, and separate fluid passages.

The geometry-preparation workflow involved:

1. Importing the heat-exchanger geometry into SimScale.
2. Creating the shell-side and tube-side flow regions.
3. Selecting the shell and both flow regions for the imprint operation.
4. Applying the geometry operation and saving the prepared assembly.
5. Preparing the geometry for conjugate heat-transfer analysis.

Correct representation of the fluid and solid domains is important for capturing heat transfer between the fluids and the heat-exchanger walls.

## 5. Material Properties

| Region                    | Material |
| Shell-side fluid          | Water |
| Tube-side fluid           | Water |
| Solid heat-exchanger wall | Steel |

The material assignments provide the physical properties required for the flow and thermal calculations. The exact property values used by SimScale depend on the selected material definitions and should be checked in the simulation setup.

## 6. Boundary Conditions

The following boundary conditions were specified for the simulation.

| Parameter        | Shell Side | Tube Side |
| Inlet temperature| 100 °C     | 80 °C |
| Inlet velocity   | −0.5 m/s   | −0.8 m/s |
| Outlet condition | Pressure outlet | Pressure outlet |
| Working fluid | Water | Water |


### Boundary-Condition Notes

- The negative inlet velocities are documented as configured. Their physical directions depend on the selected face normals and coordinate convention.
- The numerical values for the outlet pressure conditions were not provided and are therefore not assumed.
- Both inlets and outlets should be assigned to their intended fluid regions.
- Fluid–solid interfaces must be configured appropriately for conjugate heat transfer.

## 7. Mesh Generation

The geometry was meshed before the simulation was run. The mesh discretizes the computational domains into cells for the numerical solution of the governing equations.

Mesh resolution and quality affect the prediction of velocity gradients, thermal boundary layers, and heat transfer near the tube walls.

### Mesh Visualization

[View mesh image](images/mesh.png)

The mesh cell count, element-size distribution, and mesh-quality metrics were not recorded in the supplied project details. These values can be added from the SimScale mesh information if available.

## 8. Simulation Execution

After geometry preparation, material assignment, boundary-condition setup, and mesh generation, the simulation was executed in SimScale.

The simulation end time was **1,000 seconds**. Temperature contours, velocity fields, and residual histories were reviewed after the run.

### Simulation Summary

## 9. Results and Post-Processing

### 9.1 Temperature Distribution

The temperature contour visualizes the temperature field throughout the heat-exchanger model.

[View temperature contour](images/temperature-contour.png)


The contour provides a qualitative view of thermal distribution. Further checks of boundary conditions, thermal interfaces, and convergence are required before using the temperature field to calculate or validate heat-exchanger performance.

### 9.2 Velocity Distribution

The velocity contour illustrates flow distribution through the heat-exchanger passages.

[View velocity contour](images/velocity-contour.png)

The velocity field can be used to investigate flow patterns and local variations associated with the exchanger geometry. Interpretation should account for inlet directions, outlet conditions, and mesh resolution.

### 9.3 Solver Residuals

Residual histories were monitored to examine the numerical behavior of the simulation.

[View residual plot](images/residuals.png)

The supplied residual plots show that some residuals decrease initially but later rise or level off. The residual history alone does not demonstrate full convergence.

Additional assessment should include the stability of monitored temperatures and flow quantities, verification of the solver settings, and an overall energy balance.

## 10. Engineering Interpretation

The simulation provides qualitative visualizations of temperature and velocity distribution in the U-tube heat exchanger.

The main areas of investigation include:

- Temperature variation through the shell-side and tube-side passages.
- Flow distribution through the heat-exchanger geometry.
- Thermal interaction between fluid regions and solid walls.
- Numerical behavior during the 1,000-second simulation.
- The influence of geometry and boundary conditions on the computed fields.

No validated values for heat duty, overall heat-transfer coefficient, pressure drop, or exchanger effectiveness are claimed because these quantities have not been independently calculated and verified from the supplied results.

## 11. Limitations and Recommended Improvements

The following checks would strengthen the reliability of the simulation:

1. **Verify the solver type:** Confirm whether the actual simulation used a steady-state or transient solver.
2. **Check convergence:** Review residuals and confirm that important monitored quantities have stabilized.
3. **Verify flow directions:** Ensure the negative inlet velocities produce the intended flow directions.
4. **Confirm thermal interfaces:** Check that heat transfer between the water regions and steel walls is correctly represented.
5. **Review mesh quality:** Inspect cell count, mesh-quality metrics, and near-wall resolution.
6. **Perform mesh-independence testing:** Compare results from multiple mesh resolutions.
7. **Perform an energy balance:** Compare heat lost by the hot stream with heat gained by the cold stream, allowing for numerical error and external heat losses.
8. **Calculate performance metrics:** Once convergence and energy balance are satisfactory, calculate heat duty, pressure drop, and heat-transfer coefficients.
9. **Document all conditions:** Record the outlet pressure values and clarify the role of the additional 15 °C temperature.


## 12. Conclusion

This project demonstrates a CFD workflow for investigating conjugate heat transfer in a U-tube heat exchanger using SimScale. The work includes geometry preparation, flow-region creation, material assignment, boundary-condition specification, mesh generation, simulation execution, and post-processing.

The temperature and velocity contours provide qualitative insight into the computed thermal and flow fields. Further convergence assessment, mesh verification, and energy-balance calculations are needed before the results can support validated quantitative performance claims.


- **SimScale link:** [(https://www.simscale.com/projects/mehwish_akhtar/heat_transfer_in_a_u-tube_heat_exchanger_1425350692/)



