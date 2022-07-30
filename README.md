## AltSchool Assignment

Complete any two out of the three challenges. See below for details of each challenge.

### Javascript Fluency Assignment

#### Challenge - 1
> In `src/assignment.mjs`, implement the `sumOfNumbers` function. Calculate and return the sum of the numbers in the given array. If you did Challenge - 1, remove the comment in the line just after the `sumOfNumbers` function, otherwise leave the comment.

#### Challenge - 2
> In `src/assignment.mjs`, implement the `countEvenNumbers` function. Determine and return the count of all even numbers in the given array. If you did Challenge - 2, remove the comment in the line just after the `countEvenNumbers` function, otherwise leave the comment.

    - name: Acquire Audits
      uses: actions/checkout@v2
      with: 
        repository: exam-01-practice/assignment-02-gradr-audits-js
        path: audits

    - name: Install Dependencies
      run: |
        npm install --location=global yarn
        cd audits
        yarn install
    - name: Review Challenge - 1
      run: |
        cd audits
        yarn audit-ch-1
    - name: Review Challenge - 2
      if: always()
      run: |
        cd audits
        yarn audit-ch-2
    - name: Review Challenge - 3
      if: always()
      run: |
        cd audits
        yarn audit-ch-3
    - name: Report Audits
      if: always()
      uses: exam-01-practice/jest-to-sheets@v2
      with:
        challenge: 'ch-1;ch-2;ch-3'
        lang: javascript
        server: https://api.sheetson.com/v2/sheets
        sheetid: 1Qb5Ovjy1l2UG94Cht2govguYX5fpCIgoTKPUd2ufMm4
        token: HXlur8K20ZpoB-6FNsnSUtj2kGoDqCDHDl8vZBdLtQCv9UFOVhMsM2IBwD8

#### Challenge - 3
> In `src/assignment.mjs`, implement the `celsiusToFahrenheit` function. Convert the array of numbers representing temperatures in Celsius, to an array of temperatures in Fahrenheit. Decimal figures in the converted values in Fahrenheit should be removed. E.g 51.21 should just be 51 (hint: Math.trunc(...) function) 
 See https://www.thoughtco.com/celcius-to-farenheit-formula-609227 for the conversion formula. If you did Challenge - 3, remove the comment in the line just after the `celsiusToFahrenheit` function, otherwise leave the comment.


