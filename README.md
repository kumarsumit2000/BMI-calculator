﻿# BMI-calculator
JS functionality code snippet for this project
```javascript
    let form = document.querySelector("form");

    form.addEventListener("submit", (event) => {
    event.preventDefault();
    let height = parseInt(document.querySelector("#height").value);
    let weight = parseInt(document.querySelector("#weight").value);
    let result = document.querySelector("#result");

    // input checks
if(height == "" || height < 0 || isNaN(height)){
    result.textContent = `Please give a valid height ${height}`;
    result.style.color = "red";
}else if(weight == "" || weight < 0 || isNaN(weight)){
    result.textContent = `Please give a valid weight ${weight}`;
    result.style.color = "red";
}else{
     const bmi = (weight/((height * height)/10000)).toFixed(2);
    //  show the result
     result.textContent = `Your BMI Weight is: ${bmi}`;
     result.style.color = "green";
}

    })

