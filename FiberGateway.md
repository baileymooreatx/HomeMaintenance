<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [AT&T BGW320 Fiber Gateway](#att-bgw320-fiber-gateway)
  - [Service LED](#service-led)
  - [WPS LED](#wps-led)
  - [Overheating](#overheating)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# AT&T BGW320 Fiber Gateway

## Service LED

The **Service LED** on the AT&T BGW320 (All-Fi Hub) uses the following colors
and patterns to indicate its status:

| **Service LED**               | **Meaning**                                                                                             |
|:------------------------------|:--------------------------------------------------------------------------------------------------------|
| Solid White                   | Gateway is online and working normally.                                                                 |
| Blinking White (Slow)         | Gateway is powering up.                                                                                 |
| Blinking White (Fast)         | Gateway is starting up; please wait.                                                                    |
| Blinking Green (Fast)         | Gateway is connected to the network and ready for activation (initial installation only).               |
| Solid Red (WPS LED Off)       | Gateway is overheating — move it to a flat, well-ventilated surface.                                    |
| Solid Red (WPS LED Solid Red) | Hardware issue — if rebooting doesn't fix it, the gateway needs replacement.                            |
| Blinking Red (Fast)           | Network service issue; may require AT&T intervention. Check for outages and try rebooting.              |
| Blinking Red (Slow)           | No broadband connection. Check for loose/damaged cables, then hold the red reset button for 10 seconds. |
| Solid Amber                   | Gateway is powered on and starting up; wait until it turns solid white.                                 |
| Blinking Amber (Slow)         | Gateway is receiving a software update; wait until it returns to solid white.                           |
| Solid Yellow                  | A VoIP phone line is registered, or a call is in progress.                                              |
| Blinking Yellow (Fast)        | Phone registration failed, or a VoIP line has a problem.                                                |
| Blinking Blue (Fast)          | Internet outage detected; gateway is attempting to switch to internet backup mode.                      |
| Solid Blue                    | Gateway is in internet backup mode (cellular); will return to fiber when the outage ends.               |

**Note:** Some third-party guides describe the BGW320's healthy state as "solid
green," but AT&T's official documentation for this model specifies **solid white
** as the normal online indicator. The green light on the back is the separate
**Power LED**.

## WPS LED

The **WPS LED** on the AT&T BGW320 is a small light located on the **front of
the gateway**, directly below the Service LED. It is paired with the **WPS
button** (a small round button on the front, near the bottom edge) and indicates
the status of **Wi-Fi Protected Setup (WPS)** pairing — the one-button process
for connecting a new Wi-Fi device without typing in the network password.

| **WPS LED**                                 | **Meaning**                                                                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| Off                                         | WPS pairing is off. Press the WPS button to begin pairing.                                                                                     |
| Blinking Green (Slow) *(~1 blink / 2 sec)*  | The WPS button has been pressed. Take action on the Wi-Fi device you're trying to connect (press its WPS button within 2 minutes).             |
| Blinking Green (Fast) *(~2–3 blinks / sec)* | The gateway is going through a **factory reset**. Wait for it to restart.                                                                      |
| Blinking Red (Fast) *(~2–3 blinks / sec)*   | Multiple Wi-Fi devices are trying to connect at once, or the gateway has been rebooted. Wait before retrying.                                  |
| Solid Red                                   | WPS pairing **failed**. Wait for the light to change, then press the WPS button again — or connect using your Wi-Fi name and password instead. |

**How to use it:** Press the WPS button on the gateway (the light starts
blinking green slowly), then within ~2 minutes press the WPS button on the
device you want to connect (a TV, printer, etc.). Once pairing succeeds, the
light turns off.

**Note:** The WPS LED also serves as a **diagnostic companion** to the Service
LED — when the Service LED is **solid red**, the WPS LED's state tells you the
cause: **Off** = overheating, **Solid Red** = hardware fault.

## Overheating

The AT&T BGW320 uses a **heat chimney** design — cool air enters through vents
on the **bottom** and hot air exhausts through the **top**. Overheating is
triggered when that airflow is restricted or internal heat generation outpaces
it. The main causes are:

**Placement & Ventilation**

- **Confined spaces** – enclosed cabinets, closets, behind wiring panels, or
  stacked on top of other electronics.
- **Soft or obstructed surfaces** – placing the gateway on carpet, a rug, or any
  material that blocks the bottom intake vents.
- **Blocked top vents** – objects stacked on top of the unit, or the unit
  sitting in a space with no clearance above.
- **Dust buildup** – clogged ventilation holes on the top or bottom reduce
  airflow over time.

**Heat Sources**

- **High ambient temperature** – hot rooms, direct sunlight, or proximity to
  other heat-generating devices (e.g., a switch, ONT, or PC).
- **Heavy network load** – many connected devices, sustained 4K streaming, large
  downloads, or gaming can push the internal SFP/ONT modules (the main heat
  producers) into the overheat range.

**Notable details**

- The overheat alarm threshold is reportedly around **113°F (45°C)**
  internally, which is relatively low — the SFP/ONT modules generate significant
  heat and are the primary heat source, not the CPU.
- Some users on r/ATTFiber report that the solid-red "overheat" indicator can
  also appear for **low fiber light levels** or other line issues, and that
  AT&T's documentation may conflate the two. If the gateway is in a
  well-ventilated, open space and still shows solid red, the cause may be a
  fiber/line problem rather than true thermal overheating.

**Quick fixes**

1. Move the gateway to a flat, hard surface with open space around, under, and
   above it.
2. Clear dust from the top and bottom vents.
3. Keep it away from other heat-generating electronics.
4. Power-cycle the gateway (unplug 30+ seconds, plug back in) to let it cool and
   reset.
