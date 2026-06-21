# Interactive HTML BOM Linking Demo

This project was created to demonstrate the linking capabilities of the [Interactive HTML BOM](https://github.com/openscopeproject/interactivehtmlbom).

The __live demo__ found here: https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/

## Usage

You can create URL liks to __components__ and __nets__ like this:
- Link to __R1__: `ibom.html?ref=R1` -> [link](https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/?ref=R1&id=1)
- Link to __VCC__: `ibom.html?net=VCC` -> [link](https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/?net=VCC)

Because html rules there are some specia characters, like `+` or `-` symbols and so on. It is really a pain, because PCB designs often has these characters( `+3V3`, `-5V` and so on... ). For this reason some URL woodoo is needed to 'escape' these characters. For this reason a copy link button added next to each net and component name, that makes things simple.

# Designator error handling

KiCad assigns a unique identifier to every component placed on the PCB. This identifier can be used to reference a component even if its designator changes. As a result, components can be identified not only by their designator but also by their unique ID.

Unfortunately, unique IDs are usually not very descriptive ( most of the time they are just numeric values ) making them less user-friendly for everyday reference. However, they provide an important advantage: __if the PCB design changes and a component receives a new designator, links can still remain valid across revisions.__

For this reason, generated component links include both the designator and the unique identifier. If a mismatch is detected between the two, a warning dialog is displayed in the top-right corner of the screen. The user can then choose whether to open the link using the designator or the unique identifier.

Example of a broken link: [D: R2 UID: R1](https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/?ref=R2&id=1)
