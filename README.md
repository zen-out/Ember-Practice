
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->



<!-- /code_chunk_output -->

This is like main.handlebars

1. ember generate route [route]
2. class as model() {} - which returns routes (this could be
the data that you pass into the page)
3. ember generate component people-list
4. In the component, identify props
```
<h2>{{@title}}</h2>
{{#each @people as |person|}}
<li>{{person}}</li>
{{/each}}
```
5. In the page, just call the component by passing in the
variables
```
<PeopleList @title="List of Scientists"
    @people={{model}}/>
    ```

    6. Create user interactions by

    A. Embedding the logic (this is like logic.js)
    ```
    @import {action} from '@ember/object'

    @action
    showPerson(person) {
    alert(the person's name is ${person})
    }
    ```
    B. Utilizing the onclick function in handlebars (if no
    parameter)
    ```
    <button type="button" {{on 'click' this.showPerson}}>{{person}}</button>
    ```
    ```
    <button type="button" {{on 'click' this.showPerson}}>{{person}}</button>
    ```
6. 