This cluster utilizes only the intel igpu for each of it's i5-1240p cpu's.

Notes:
i5-1240p supports 7 VF's
My cluster explicitly uses the xe drivers and not the i915 drivers because the i5-1240p supports both
  - i915 is loaded, but blacklisted so that the xe drivers can use The intel Graphics Micro Controller (GuC).
  - xe is explicitly used because the SR-IOV functionality is only in the xe drivers for Alder Lake
Intels Resource Driver for DRA dynamically assigns the VF's to any workload that calls it
I explicitly have set it up this way so I do not have to assign adminAccess to each namespace allowed to provision GPU's to workloads
