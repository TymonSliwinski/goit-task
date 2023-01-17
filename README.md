# GoIT task

[Task 1 - stringBuilder](#task-1)  
[Task 2 - box creator](https://tymonsliwinski.github.io/box-creator/)  
[Task 3 - infinite scroll](https://tymonsliwinski.github.io/infinite-scroll/)

## Task 1 - stringBuilder <a id='task-1'></a>
I'm just going to include this here, since there's no need to create a separate page for it.

```js
/** 
 * Class for building strings
 * @extends String
 */
class StringBuilder extends String {
    /**
     * initializes StringBuilder with baseString
     * @param {string} baseString initial string 
     */
    constructor(baseString = '') {
        super(baseString);
        this.value = baseString;
    }

    // override toString method for console.log display
    toString() {
        return this.value;
    }

    /**
    * @param {string} str string to append to the end
    * @returns {StringBuilder}
    * */
    append(str = '') {
        this.value = this.value + str;
        return this;
    }

    /**
     * @param {string} str string to prepend to the beginning
     * @returns {StringBuilder}
     * */
    prepend(str = '') {
        this.value = str + this.value;
        return this;
    }

    /**
     * @param {string} str string to pad from both sides
     * @returns {StringBuilder}
     */
    pad(str = '') {
        this.value = str + this.value + str;
        return this;
    }

}

const builder = new StringBuilder('.');

builder
    .append('^')
    .prepend('^')
    .pad('=');

console.log(builder); // '=^.^='
```