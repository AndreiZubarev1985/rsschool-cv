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

```
module.exports = function multiply(first, second) {
        const product = Array(first.length+second.length).fill(0);
        for (let i = first.length; i--; null) {
            let carry = 0;
            for (let j = second.length; j--; null) {
                product[1+i+j] += carry + first[i]*second[j];
                carry = Math.floor(product[1+i+j] / 10);
                product[1+i+j] = product[1+i+j] % 10;
            }
            product[i] += carry;
            console.log(product);
        }
        if(product[0] === 0) {
            let result = product.shift();
            return product.join('');
        } else {
            return product.join('');
        }
    };
    
```



- Education

Professional development, courses:
    
    1. Educational center of HTP, Web Development (2013): HTML, CSS, JavaScript, MySql
    2. HTMLAcademy:  HTML, CSS basics (2019)

- English language skills:

B1- Intermediate