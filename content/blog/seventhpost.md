---
title: All about 'Loops, Arrays and Objects'
description: In the last month I've plunged into the world of JavaScript - here's a snapshot of what I've learnt.
date: 2024-08-01
tags:
  - number 7
  - loops
  - arrays
  - objects
  - javascript
---

Objects, objects, objects - Javascript is all about objects. In fact you'd be hard pressed to find anything escaping the definition of object. W3, all hail, tells us that only 'primitive' values and data types such as your strings, numbers etc qualify as such. 

Using objects, arrays and loops - I will not only be sharing my chicken soup recipe with you - but also the method I am using to bring it to life.

First, I declare my object and populate it with the key:value pairs that I need.

```js
// this is an object, note it's curly braces and key:value format.
const chickenSoupRecipe = {
    title: "Chicken Soup",
    servings: 4,
    ingredients: ['400g of chicken breast','4 stalks of celery','3 carrots','1 large potato','1 brown onion','5 cloves of garlic','Fresh rosemary','Fresh parsley', '500ml of chicken stock'],
    directions: ['Dice the celery, carrots, potato and brown onion. Mince the garlic and prepare your stock', 'In a large pot saute your carrots, celery and onion until fragrant and soft.',
                    'Then add your stock, potato, garlic and rosemary and bring to a simmer','Once simmering, add your chicken breasts and cook at a low-medium heat for 10 minutes.',
                    'Remove and shred the chicken breast, return it to the pot and continue simmering for 30 minutes.',
                    'At this point you can serve up, but for extra flavour leave at a low heat for another 30-50 minutes. Serve with a squeeze of fresh lemon, and stir in your fresh parsley.']
    
    }
```

Now that my object is declared - I am going to create a function that logs the recipe, looping through the 'ingredients' and 'directions' array. 

```js
//this is a function, note the 'recipe' parameter through, allowing me to pass through any future recipe.
function describeRecipe (recipe) {
    console.log(`${recipe.title}`);
    console.log(`This recipe serves ${recipe.servings}.`);
    console.log(`Ingredients:`)
    for (const ingredient of chickenSoupRecipe.ingredients) {
        console.log(`- ${ingredient}`);
    }
    console.log(`Method:`);
    for (const direction of chickenSoupRecipe.directions) {
        console.log(direction)
    }
}
```

With my function created, all that's left for me to do is call the function and receive my recipe!

```js
describeRecipe(chickenSoupRecipe)
```

All of this outputs to:

"Chicken Soup"

"This recipe serves 4."

"Ingredients:"

"- 400g of chicken breast"

"- 4 stalks of celery"

"- 3 carrots"

"- 1 large potato"

"- 1 brown onion"

"- 5 cloves of garlic"

"- Fresh rosemary"

"- Fresh parsley"

"- 500ml of chicken stock"

"Method:"

"Dice the celery, carrots, potato and brown onion. Mince the garlic and prepare your stock"
"In a large pot saute your carrots, celery and onion until fragrant and soft."
"Then add your stock, potato, garlic and rosemary and bring to a simmer"
"Once simmering, add your chicken breasts and cook at a low-medium heat for 10 minutes."
"Remove and shred the chicken breast, return it to the pot and continue simmering for 30 minutes."
"At this point you can serve up, but for extra flavour leave at a low heat for another 30-50 minutes. Serve with a squeeze of fresh lemon, and stir in your fresh parsley."


And there you have it! Chicken soup, objects and arrays - what a combination. 



