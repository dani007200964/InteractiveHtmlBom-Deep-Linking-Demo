# Interactive HTML BOM Linking Demo

This project was created to demonstrate the linking capabilities of the [Interactive HTML BOM](https://github.com/openscopeproject/interactivehtmlbom).

The __live demo__ found here: https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/

## Usage

You can create URL liks to __components__ and __nets__ like this:
- Link to __R1__: `ibom.html?ref=R1` -> [link](https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/?ref=R1)
- Link to __VCC__: `ibom.html?net=VCC` -> [link](https://dani007200964.github.io/InteractiveHtmlBom-Deep-Linking-Demo/?ref=R1&net=VCC)

Because html rules there are some specia characters, like `+` or `-` symbols and so on. It is really a pain, because PCB designs often has these characters( `+3V3`, `-5V` and so on... ). For this reason some URL woodoo is needed to 'escape' these characters. For this reason a copy link button added next to each net and component name, that makes things simple.
