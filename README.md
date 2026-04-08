# Heated Square Cylinder Case

This OpenFOAM case models steady forced convection over a square cylinder with a constant heat flux applied to the cylinder surface.

## Files
- `system/blockMeshDict`: 2D mesh around a square cylinder obstacle
- `system/controlDict`: steady-state solver control settings
- `system/fvSchemes`, `system/fvSolution`: discretization and solver settings
- `constant/transportProperties`, `constant/thermophysicalProperties`, `constant/turbulenceProperties`: fluid and thermal properties
- `0/U`, `0/p_rgh`, `0/T`: initial and boundary fields

## Running the case
1. Open a terminal in this folder.
2. Run `blockMesh`.
3. Run `buoyantSimpleFoam`.

## Notes
- The cylinder heat flux is set in `0/T` for patch `cylinder`.
- Change the inlet velocity in `0/U` and the heat flux in `0/T` to study different cases.
- This is a 2D `empty`-plane configuration with thickness `0.01 m` in the z-direction.
