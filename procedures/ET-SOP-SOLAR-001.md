# Solar Panel No-Charge Troubleshooting SOP

| | |
|---|---|
| **Document ID:** | ET-SOP-SOLAR-001 |
| **Company:** | Escape Trailer |
| **Revision:** | 1.0 |

---

## Tools Required

- [ ] Multimeter (DC volts + continuity mode)
- [ ] MC4 disconnect tool (or pliers)
- [ ] Flashlight

---

## ⚠️ Safety

- [ ] **Test in daylight** — panels are live when exposed to light
- [ ] **Cover panel with opaque blanket** to de-energize before working on connections
- [ ] **Disconnect battery negative** before working on charge controller wiring

---

## Troubleshooting Steps

> **Follow sequentially. Stop when fault is found → go to Disposition.**

### Step 1: Panel Output Test
- [ ] Disconnect panel leads from charge controller
- [ ] Measure DC voltage across panel +/- leads
- [ ] **Expected:** 18–22V open circuit (12V system) in decent light
- **FAIL (0V):** Panel fault or connector issue → inspect panel surface & junction box
- **PASS:** Proceed to Step 2

### Step 2: MC4 Connector Inspection
- [ ] Disconnect MC4 connectors on roof
- [ ] Visual check: corrosion (green/white deposits), moisture, bent pins
- [ ] Clean or replace if corroded
- [ ] Reconnect and retest voltage downstream
- **FAIL:** Replace/clean connectors, retest
- **PASS:** Proceed to Step 3

### Step 3: Roof Junction Box
- [ ] Open junction box on panel
- [ ] Inspect for water ingress / corrosion
- [ ] Check wire terminations — loose, corroded, melted
- [ ] Continuity test through junction connections
- **FAIL:** Repair/replace junction box components
- **PASS:** Proceed to Step 4

### Step 4: Inline Fuse Check
- [ ] Locate inline fuse between panel and charge controller
- [ ] Visual inspection of fuse element
- [ ] Continuity test across fuse
- **FAIL:** Replace fuse (note amperage rating)
- **PASS:** Proceed to Step 5

### Step 5: Wire Run Continuity
- [ ] Disconnect both ends of wire run (roof to controller)
- [ ] Continuity test: **positive wire** end-to-end → should beep ✓
- [ ] Continuity test: **negative wire** end-to-end → should beep ✓
- [ ] Cross test: **positive to negative** → should NOT beep ✗ (short if it does)
- **FAIL:** Damaged wire — trace and repair/replace
- **PASS:** Proceed to Step 6

### Step 6: Charge Controller Input
- [ ] Reconnect panel to controller
- [ ] Check controller display for solar input voltage
- **0V with good panel:** Wiring fault upstream — repeat Steps 2–5
- **Voltage but 0 amps:** Controller fault or battery full/disconnected
- **PASS:** Proceed to Step 7

### Step 7: Charge Controller Fuse
- [ ] Locate controller's solar input fuse (if equipped)
- [ ] Continuity test across fuse
- **FAIL:** Replace controller fuse
- **PASS:** Proceed to Step 8

### Step 8: Battery Connection
- [ ] Verify battery terminals tight, no corrosion
- [ ] Check battery voltage (if fully charged, controller may show 0 amps — normal)
- [ ] Check battery fuse / disconnect switch is closed
- **FAIL:** Repair battery connections / replace fuse
- **PASS:** No fault found → see Disposition

---

## Result Recording

| Step | Result (Pass/Fail) | Notes | Inspector | Date |
|:----:|:------------------:|:------|:---------:|:----:|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |
| 4 | | | | |
| 5 | | | | |
| 6 | | | | |
| 7 | | | | |
| 8 | | | | |

---

## Disposition

- [ ] **Fault found & repaired** → Retest from Step 1 to confirm charging
- [ ] **No fault found** → Escalate to electrical lead
- [ ] **Document all findings on trailer work order**

---

## Inspector Sign-Off

| | |
|:---|:---|
| **Inspector Name:** | __________________ |
| **Date:** | __________________ |
| **Trailer Serial #:** | __________________ |
| **Work Order #:** | __________________ |

---

*Escape Trailer — Quality Control Documentation*
