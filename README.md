# &lt;multi-input&gt;

<img width="340" alt="multi-input custom element showing selection of multiple Shakespeare characters" src="https://user-images.githubusercontent.com/205226/59288731-5744e400-8c6c-11e9-8b8d-4212d4504c86.png">

Custom element for selecting multiple items using an `input` and `datalist` to suggest options.

Delete items with Backspace or by tapping/clicking an item's × icon.

<br>

| [View and remix this project live on Glitch](https://glitch.com/~multi-input) |
| --- |

<br>

## Usage

1. Add _multi-input.js_ to your project and link to it: 

    ```html
    <script src="multi-input.js"></script>
    ```

2. Wrap an `input` and a `datalist` in a `<multi-input>` (see [index.html](https://glitch.com/edit/#!/multi-input?path=index.html:14:0)): 

    ```html
    <multi-input>
      <input list="speakers">
      <datalist id="speakers">
        <option value="Banquo"></option>
        <option value="Celia"></option>
        ...
      </datalist>
    </multi-input>
    ```
 
3. Get selected values like this (see [script.js](https://glitch.com/edit/#!/multi-input?path=script.js:4:0)):

    ```js
    const getButton = document.getElementById('get');
    const multiInput = document.querySelector('multi-input'); 
    getButton.onclick = () => {
      console.log(multiInput.getValues());
    }
    ```
<br>
    
## My platform doesn't support custom elements :^|

Custom elements are [widely supported by modern browsers](https://caniuse.com/#search=custom%20elements).

However, `<multi-input>` the  custom element wraps an `input` element that has a `datalist`, so behaviour will fall back naturally to a 'normal' `datalist` experience.

<br>
    
## My platform doesn't support datalist :^|&nbsp;:^|

The `datalist` element is [supported by all modern browsers](https://caniuse.com/#feat=datalist).

If your target browser doesn't support `datalist`, behaviour will fall back to the plain old `input` experience.

<br>

## Obligatory screencast

<img src="https://cdn.glitch.com/dda744c5-58a9-4809-897c-68396377983a%2Fmulti-input.gif?v=1560266060751" alt="Screencast showing Shakespeare character names being selected via a multi-input custom element" width="400">
