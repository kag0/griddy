* Wrap content in a grid.

    ```html
    <div class="grid">
    </div>
    ```

* All and only direct children are gridded
    * This means that grids can be nested without outer grids interfering with inner grids. 

    ```html
    <div class="grid">
        <div>item1</div>
        <div>item2</div>
        <div>item3</div>
    </div>
    ```

* By default each grid square is 1/12th of the grid. In other words, it's a 12x12 grid layout. Specify if a square should be larger like this

    ```html
    <div class="grid">
        <div class="x-5"></div>
        <div class="x-2">item2</div>
        <div class="x-5"></div>
    </div>
    ```

* The grid is responsive; so adding more than 12 squares will cause additional content to wrap, and the grid will collapse to be one column in spaces less than `60em`

* If a square should dissapear on smaller screens, give it the `spacer` class.

    ```html
    <div class="grid">
        <div class="x-5 spacer"></div>
        <div class="x-2">item2</div>
        <div class="x-5 spacer"></div>
    </div>
    ```

* Squares can be made larger vertically as well as horizontally.

    ```html
    <div class="grid">
        <div class="x-6 y-2">item1</div>
        <div class="x-6">item2</div>
        <div class="x-6">item3</div>
    </div>
    ```

* If a large vertical square should have a different height on small screens, give it a `y-collapse` class.

    ```html
    <div class="grid">
        <div class="x-3 y-2 y-collapse">item1</div>
        <div class="x-3">item2</div>
        <div class="x-3">item3</div>
        <div class="x-3 y-2 y-collapse">item4</div>
        <div class="x-3">item5</div>
        <div class="x-3">item6</div>
    </div>
    ```

* To make grid squares expand to fill any available space in the grid, make the grid `fit-columns` and `fit-rows`.

    ```html
    <div class="grid fit-columns">
        <div>left/top</div>
        <div>right/bottom</div>
    </div>
    ```

* The ["holy grail"](https://en.wikipedia.org/wiki/Holy_grail_(web_design)) layout can be [easily implemented](grail.html) this way.