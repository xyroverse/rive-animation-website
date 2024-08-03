# Rive Animation Website

This repository contains the Rive animation files for Xyro, LLC branded logo animations hosted publicly for website to have direct access.

## Installation

Clone this repo using the following git url:

```text
https://github.com/xyroverse/rive-animation-website.git
```

Clone this repo using the GitHub CLI gh repo clone xyroverse/rive-animation-website:

```text
gh repo clone xyroverse/rive-animation-website
```

## Usage

### Xyro Animations

Xyro Icon:
`xyro_logo_anim_letters_bounce_in.riv`

Xyro Logo:
`xyro_logo_anim_all_text_slideup.riv`
`xyro_logo_anim_letters_bounce_in.riv`

Xyro Horizontal Logo:
`xyro_logo_anim_letters_bounce_in.riv`

### Embed into Web Page

Embed Rive animation in a web page using the specific file's permalink

```html
<div style="display: flex; justify-content: center; align-items: center; width: 100%; height: 100%; overflow: hidden">
<canvas id="canvas" style="display: flex; width: 100%; height: 100%; overflow: hidden;"></canvas>
</div>
<script src="https://unpkg.com/@rive-app/canvas@2.19.6"></script>
<script>
      const r = new rive.Rive({
  src: "https://raw.githubusercontent.com/xyroverse/rive-animation-website/5376c095437d874f1e53d67116aed25797baef9f/xyro_logo_anim_letters_bounce_in.riv",
  canvas: document.getElementById("canvas"),
  stateMachines: "State Machine 3",
  autoplay: true,
  onLoad: () => {
    r.resizeDrawingSurfaceToCanvas();
    const canvas = document.getElementById("canvas");
    canvas.addEventListener("click", () => {
      const input = r.stateMachineInputs("State Machine 3").find(i => i.name === "OnClick");
      if(input) {
        input.fire();
      }
    });
  }
});
</script>
```

## Packages

This repo utilizes the animation technologies via Rive:

[https://rive.app/](https://rive.app/)

This repo utilizes the Rive package:

- [ ] npm i @rive-app/canvas

[https://github.com/rive-app/rive-wasm/tree/master](https://github.com/rive-app/rive-wasm/tree/master)

## License

This animation is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.

## Trademark Notice

The logo included in this repository is a trademark of Xyro, LLC and is protected by trademark law. The logo may not be used in any form without prior written permission from Xyro, LLC.

Any use of the logo in the Rive animation or any other content in this repository is subject to the following conditions:

1. The logo may only be used as intended within the context of this repository.
2. The logo must not be altered, modified, or used out of context.
3. Any distribution or use of the logo outside of this repository requires explicit permission from Xyro, LLC.

For permissions or further inquiries, please contact legal@xyroverse.com.
