---
title: 3 ways to loop over Object properties with Vanilla JavaScript
date: 2017-09-21T18:59:43.000Z
description: >-
  It happens a lot that you need to loop over an Array with JavaScript Objects!
  But sometimes you just don’t know what kind of properties that Object has.
  Lucky we are that JavaScript offers a few ways of looping over JavaScript
  Object properties.
image: /img/how-to-check-equality-of-values-in-javascript-1024x576.jpg
---
It happens a lot that you need to loop over an Array with JavaScript Objects! But sometimes you just don’t know what kind of properties that Object has. Lucky we are that JavaScript offers a few ways of looping over JavaScript Object properties.

I wanted to share 3 of them with you. So hopefully this will help you in the right direction.

## The Object to loop over

First, we need an example object to loop over. So I put some of my experience in it 😉 (hahaha)! Keep the fun in it!

<pre>let experienceObject = {
    name: 'Raymon',
    title: 'Lead Frontend/JavaScript Developer',
    yearsExperience: 8,
    projects: [
        {
            name: 'ANWB',
            title: 'Senior JavaScript Developer',
            techniques: ['Angular', 'ES6', 'Vanilla JavaScript', 'Less', 'CSS']
        },
        {
            name: 'NATO',
            title: 'Lead JavaScript Developer',
            techniques: ['Angular 2', 'AngularJS', 'ES6', 'Vanilla JavaScript', 'Web Sockets', 'D3']
        },
        {
            name: 'Rabobank',
            title: 'Senior Frontend Developer',
            techniques: ['Vanilla JavaScript', 'CSS', 'Responsive Webdesign']
        }
    ]
}
</pre>

## Object.keys(experienceObject).map()

The first example is the Object.keys map method to loop over the properties of the Object it.

<pre>Object.keys(experienceObject).map(e =&gt; {
    console.log(`key= ${e} value = ${experienceObject[e]}`)
});
</pre>

## Object.entries(experienceObject).forEach()

The second example is the Object.keys with the forEach method over the properties of the Object it.

<pre>Object.entries(experienceObject).forEach(([key, value]) =&gt; {
    console.log(`key= ${key} value = ${value}`)
})
</pre>

## For-in loop

The last example is the For-in loop to loop over the properties of the Object it.

<pre>for (property in experienceObject) {
  console.log(`key= ${property} value = ${experienceObject[property]}`)
}
</pre>

## Check the console output

[JS Bin on jsbin.com](http://jsbin.com/qusaguf/1/embed?console)
