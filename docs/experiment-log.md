# Experiment log

## 2026-10-10: Capacity reduction proof of concept

**Target:** Axiom C565n 500 GB, SM2259XT, Micron N28A QLC.  
**MPTool:** SM2259XT MPTool S1120A, firmware S1120A0.  
**Manual LBA:** `488281250` sectors at 512 bytes/sector.  
**MPTool outcome:** Blue `Pass! Firmware: S1120A0 (IMN28R)`.  
**After power cycle:** Windows Disk Management reported 232.83 GiB, disk uninitialized.  
**After GPT + NTFS format:** `FrankenSSD (F:)`, approximately 232.81 GiB volume.  
**Integrity check:** H2testw completed full write/read verification with ZERO errors. PASS.
### Lessons learned

- MPTool did not enumerate the drive when attached through an ASM1166 SATA controller passed to a Windows VM; native SATA on Windows 11 worked.
- Windows initially showed the old capacity immediately after flashing; a reboot/power cycle revealed the updated geometry.
- This confirms the *advertised capacity* can be changed with this tool/configuration. It does **not** establish that added NAND will be supported.

## Next entries

- [x] Record H2testw results (PASS, zero errors; elapsed time not recorded)- [ ] Restore 500 GB and validate detection
- [ ] Identify actual passive-component footprints on empty NAND sites
- [ ] Identify BGA package pitch/ball map
- [ ] Perform donor removal/reball trial
- [ ] Transplant on sacrificial receiver
- [ ] MPTool flash enumeration and full integrity test
