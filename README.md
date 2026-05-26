# DIY Lithophane Lamp

A backlit 3D-printed lithophane lamp with custom electronics — combines FDM printing with a hand-wired LED driver circuit including PWM dimming.

![License](https://img.shields.io/badge/license-MIT-green) ![3D Printing](https://img.shields.io/badge/3D%20Printing-Bambu%20Lab%20A1-brightgreen) ![Electronics](https://img.shields.io/badge/Electronics-DIY-orange)

---

## What is a Lithophane?

A lithophane is a 3D-printed panel of varying thickness — thin areas let light through (bright), thick areas block it (dark). Without backlighting it looks like an opaque green slab. With light behind it, a detailed image or pattern emerges.

---

## Hardware

### Electronics
| Component | Model / Spec |
|---|---|
| LED | 10W COB LED |
| Power Supply | Meanwell LPV-20-12 (12V, ~1.67A) |
| Heatsink | Fischer Elektronik |
| Dimmer | PWM dimmer module |

### 3D Printing
| Setting | Value |
|---|---|
| Printer | Bambu Lab A1 |
| Material | PLA (white) |
| Key parameter | Wall thickness controls light transmission |

---

## Printing the Lithophane

1. Generate your lithophane from an image using a slicer plugin or a tool like [ItsLitho](https://itslitho.com/) / Cura's lithophane post-processing script.
2. Print **vertically** (standing up) for best layer-light interaction.
3. **Thinner walls = more light** — tune wall count to control contrast.
4. Green PLA gives a warm tinted glow; white PLA gives a neutral output.

---

## Wiring

```
230V AC ──► Meanwell LPV-20-12 ──► PWM Dimmer ──► COB LED + Heatsink
                  (12V DC out)
```

> The Meanwell PSU deals with mains voltage. Make sure everything is properly insulated and enclosed before powering on.

**Heatsink sizing:** A 10W COB LED generates significant heat. The Fischer Elektronik heatsink keeps junction temperature in a safe range. Thermal paste between LED and heatsink is recommended.

---

## Tips & Lessons Learned

- **PWM dimmer whine:** Some PWM modules produce an audible whine at certain frequencies. Try a different frequency setting or replace the module if it's bothersome.
- **Brightness limiting:** If the COB runs too hot even with the heatsink, reduce max brightness via the PWM duty cycle rather than relying solely on the heatsink.
- **PSU hum:** The Meanwell LPV-20-12 may produce a faint hum under load — this is normal but can be reduced by mounting it on a vibration-dampening surface.
- **Enclosure:** An enclosure (also 3D-printed) with ventilation slots prevents dust buildup on the COB and diffuses light more evenly behind the lithophane panel.

---

## Files

```
/stl/          → 3D printable parts (enclosure, panel frame, mount)
/img/          → Photos of the finished lamp
/wiring/       → Wiring diagram
```

---

## 📸 Result

> *Add your photo here*

---

## 📄 License

MIT — do whatever you want with it, a star is appreciated. ⭐
