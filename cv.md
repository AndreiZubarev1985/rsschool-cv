# CV

- Andrei Zubarev

- E-mail: andreizubarev1985@gmail.com

- Summary

- Basic Skills: 

    1. Langugage: JavaScript, HTML, CSS (preprocessors: SASS). 
    2. Frameworks: Bootstrap, React.js (initial level).
    3. Deploy: GitHub.

- My code examples are here: 

GitHub: https://github.com/AndreiZubarev1985

```html
 
let numbers = document.querySelectorAll('.numbers'),
    operations = document.querySelectorAll('.operations'),
    specialOperations = document.querySelectorAll('.special-operations'),
    clearBtns = document.querySelectorAll('.clear'),
    display = document.getElementById('display'),
    memoryCurrentNumber = 0,
    memoryNewNumber = false,
    memoryPendingOperation = '';


for(let i = 0; i < numbers.length; i++) {
    let number = numbers[i];
    number.addEventListener('click', function(e) {

        numberPress(e.target.textContent);

    });
}

for(let i = 0; i < operations.length; i++) {
    let operation = operations[i];
    operation.addEventListener('click', function(e) {

        operationPress(e.target.textContent);

    });
}

for(let i =0; i < specialOperations.length; i++) {
    let specialOperation = specialOperations[i];
    specialOperation.addEventListener('click', function(e) {
       console.log(e.srcElement.id);
        specialOperationPress(e.srcElement.id);
    });
}


for(let i = 0; i < clearBtns.length; i++) {
    let clear = clearBtns[i];
    clear.addEventListener('click', function(e) {
        clearPress(e.srcElement.id);
    });

}



function numberPress(number) {
    if(memoryNewNumber) {
        display.value = number;
        memoryNewNumber = false;
    } else {
        if(display.value === '0') {
            display.value = number;
        } else {
            if(display.value.length > 9) { // ограничиваем количество цифр в инпуте от нажатия кнопок
                display.value = '  Error!!!   ';
            } else {
                display.value += number;
            }


        }
    }
}

function operationPress(operation) {
        let localOperationMemory = display.value;

        if(memoryNewNumber && memoryPendingOperation != '=') {
            display.value = memoryCurrentNumber;

        } else        
        {
            memoryNewNumber = true;
            if(memoryPendingOperation === '+') {
                memoryCurrentNumber += parseFloat(localOperationMemory); 
            }  else if(memoryPendingOperation === '-') {
                memoryCurrentNumber -= parseFloat(localOperationMemory);
            }  else if(memoryPendingOperation === '*') {
                memoryCurrentNumber *= parseFloat(localOperationMemory);
            }  else if(memoryPendingOperation === '/') {
                memoryCurrentNumber /= parseFloat(localOperationMemory);
            }  else {
                memoryCurrentNumber = parseFloat(localOperationMemory);
            } 
            display.value = memoryCurrentNumber;
            memoryPendingOperation = operation;
        }
};

function clearPress(id) {
    if(id == 'ce') {
        display.value = 0;
        memoryNewNumber = true;
    } else if(id = 'c') {
        display.value = 0;
        memoryCurrentNumber = 0,
        memoryNewNumber = true,
        memoryPendingOperation = '';
    } 
};

function specialOperationPress(id) {
    let temperValue = display.value;
    display.value = memoryCurrentNumber;

    if(id == 'x2') {
       display.value = temperValue*temperValue;
       memoryNewNumber = true;
    } else if(id == '1/x') {
        display.value = 1/temperValue;
    } else if(id == 'sqrt') {
        display.value = Math.sqrt(temperValue);
    } 
};
```



- Education

Professional development, courses:
    
    1. Educational center of HTP, Web Development (2013): HTML, CSS, JavaScript, MySql
    2. HTMLAcademy:  HTML, CSS basics (2019)

- English language skills:

B1- Intermediate