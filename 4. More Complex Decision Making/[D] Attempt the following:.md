# [D] Attempt the following:

(a) Any year is entered through the keyboard, write a program to determine whether the year is leap or not. Use the logical operators **&&** and **||**.

````c
#include<stdio.h>
int main(){
    int year;
    printf("Enter year : ");
    scanf("%d", &year);
    if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0){
        printf("Leap Year");
    }
    else{
        printf("Not a Leap Year");
    }
    return 0;
}
````

(b) Any character is entered through the keyboard, write a program to determine whether the character entered is a capital letter, a small case letter, a digit or a special symbol.
The following table shows the range of ASCII values for various characters:

| Characters      | ASCII Values                        |
| --------------- | ----------------------------------- |
| A - Z           | 65 - 90                             |
| a - z           | 97 - 122                            |
| 0 - 9           | 48 - 57                             |
| special symbols | 0 - 47, 58 - 64, 91 - 96, 123 - 127 |

````c
#include<stdio.h>
int main(){
    char c;
    int n;
    printf("Enter a character : ");
    scanf("%c", &c);
    n = c;
    if(n >= 65 && n <= 90){
        printf("Capital");
    }
    else if(n >= 97 && n <= 122){
        printf("Small");
    }
    else if(n >= 48 && n <= 57){
        printf("Digit");
    }
    else if(n < 128){
        printf("Special symbol");
    }
    else{
        printf("Out of range character");
    }
    return 0;
}
````

(c) A certain grade of steel is graded according to the following conditions:

(i)Hardness must be greater than 50

(ii)Carbon content must be less than 0.7

(iii)Tensile strength must be greater than 5600

The grades are as follows:

Grade is 10 if all three conditions are met

Grade is 9 if conditions (i) and (ii) are met

Grade is 8 if conditions (ii) and (iii) are met

Grade is 7 if conditions (i) and (iii) are met

Grade is 6 if only one condition is met

Grade is 5 if none of the conditions are met

Write a program, which will require the user to give values of hardness, carbon content and tensile strength of the steel under consideration and output the grade of the steel.

````c
#include<stdio.h>
int main(){
    int h,ts;
    float cc;
    printf("Enter Hardness, Carbon content, Tensile strength : ");
    scanf("%d%f%d", &h, &cc, &ts);
    if(h >= 50 && cc <= 0.7 && ts >= 5600){
        printf("Grade 10");
    }
    else if(h >= 50 && cc <= 0.7 && ts < 5600){
        printf("Grade 9");
    }
    else if(h < 50 && cc <= 0.7 && ts >= 5600){
        printf("Grade 8");
    }
    else if(h >= 50 && cc > 0.7 && ts >= 5600){
        printf("Grade 7");
    }
    else if(h >= 50 || cc <= 0.7 || ts >= 5600){
        printf("Grade 6");
    }
    else{
        printf("Grade 5");
    }
    return 0;
}
````

(d) If the three sides of a triangle are entered through the keyboard, write a program to check whether the triangle is valid or not. The triangle is valid if the sum of two sides is greater than the largest of the three sides.

````c
#include<stdio.h>
int main(){
    int a, b, c, largest;
    printf("Enter 3 sides of Triangle : ");
    scanf("%d%d%d", &a, &b, &c);
    largest = (a > b ? (a > c ? a : c) : ( b > c ? b : c));
    if((a + b) > largest || (b + c) > largest || (a + c) > largest){
        printf("Valid");
    }
    else{
        printf("Invalid");
    }
    return 0;
}
````

(e) If the three sides of a triangle are entered through the keyboard, write a program to check whether the triangle is isosceles, equilateral, scalene or right angled triangle.

````c
#include<stdio.h>
int main(){
    int a, b, c;
    printf("Enter 3 sides of Triangle : ");
    scanf("%d%d%d", &a, &b, &c);
    if(a == b && b == c && a == c){
        printf("Equilateral");
    }
    else if((a == b && a != c) || (b == c && b != a) || ( a== c && a != b)){
        printf("Isosceles");
    }
    else if(a*a + b*b == c*c || c*c+ b*b == a*a || a*a + c*c == b*b){
        printf("Right Angled");
    }
    else{
        printf("Scalene");
    }
    return 0;
}
````

(f) In boxing the weight class of a boxer is decided as per the following table. Write a program that receives weight as input and prints out the boxer’s weight class.

| Boxer Class   | Weight in Pounds |
| ------------- | ---------------- |
| Flyweight     | < 115            |
| Bantamweight  | 115 - 121        |
| Featherweight | 122 - 153        |
| Middleweight  | 154 - 189        |
| Heavyweight   | >= 190           |

````c
#include<stdio.h>
int main(){
    int wt;
    printf("Enter weight : ");
    scanf("%d", &wt);
    if(wt < 115){
        printf("Flyweight");
    }
    else if(wt >= 115 && wt <= 121){
        printf("Bantamweight");
    }
    else if(wt >= 122 && wt <= 153){
        printf("Featherweight");
    }
    else if(wt >= 154 && wt <= 189){
        printf("Middleweight");
    }
    else{
        printf("Heavyweight");
    }
    return 0;
}
````

(g) In digital world colors are specified in Red-Green-Blue (RGB) format, with values of R, G, B varying on an integer scale from 0 to 255. In print publishing the colors are mentioned in Cyan-Magenta-Yellow-Black (CMYK) format, with values of C, M, Y, and K varying on a real scale from 0.0 to 1.0. Write a program that converts RGB color to CMYK color as per the following formulae:

<img src="https://render.githubusercontent.com/render/math?math=White = Max(Red/255, Green/255, Blue/255)">

<img src="https://render.githubusercontent.com/render/math?math=Cyan = (\frac{White - Red/255}{White})">

<img src="https://render.githubusercontent.com/render/math?math=Magenta = (\frac{White - Green/255}{White})">

<img src="https://render.githubusercontent.com/render/math?math=Yellow = (\frac{White - Blue/255}{White})">

<img src="https://render.githubusercontent.com/render/math?math=Black = 1 - White">

Note that if the RGB values are all 0, then the CMY values are all 0 and the K value is 1.

````c
#include<stdio.h>
int main(){
    int r, g, b;
    float c, m, y, k, w, rm, gm, bm;
    printf("Enter RGB values : ");
    scanf("%d%d%d", &r, &g, &b);
    rm = r / 255.0;
    gm = g / 255.0;
    bm = b / 255.0;
    w = (rm > gm ? (rm > bm ? rm : bm) : (gm > bm ? gm : bm));
    c = (w - rm) / w;
    m = (w - gm) / w;
    y = (w - bm) / w;
    k = 1 - w;
    if (r == g == b == 0){
        c = 0;
        m = 0;
        y = 0;
        k = 1;
    }
    printf("%f %f %f %f", c, m, y, k);
    return 0;
}
````

(h) Write a program that receives month and date of birth as input and prints the corresponding Zodiac sign based on the following table:

| Sun Sign    | From - To                 |
| ----------- | ------------------------- |
| Capricorn   | December 22 - January 19  |
| Aquarius    | January 20 - February 17  |
| Pisces      | February 18 - March 19    |
| Aries       | March 20 - April 19       |
| Taurus      | April 20 - May 20         |
| Gemini      | May 21 - June 20          |
| Cancer      | June 21 - July 22         |
| Leo         | July 23 - August 22       |
| Virgo       | August 23 - September 22  |
| Libra       | September 23 - October 22 |
| Scorpio     | October 23 - November 22  |
| Sagittarius | November 22 - December 21 |

````c
#include<stdio.h>
int main(){
    int d, m;
    printf("Enter date & month : ");
    scanf("%d%d", &d, &m);
    if(m == 12 && d >= 22 || m == 1 && d <= 19){
        printf("Capricorn");
    }
    if(m == 1 && d >= 20 || m == 2 && d <= 17){
        printf("Aquarius");
    }
    if(m == 2 && d >= 18 || m == 3 && d <= 19){
        printf("Pisces");
    }
    if(m == 3 && d >= 20 || m == 4 && d <= 19){
        printf("Aries");
    }
    if(m == 4 && d >= 20 || m == 5 && d <= 20){
        printf("Taurus");
    }
    if(m == 5 && d >= 21 || m == 6 && d <= 20){
        printf("Gemini");
    }
    if(m == 6 && d >= 21 || m == 7 && d <= 22){
        printf("Cancer");
    }
    if(m == 7 && d >= 23 || m == 8 && d <= 22){
        printf("Leo");
    }
    if(m == 8 && d >= 23 || m == 9 && d <= 22){
        printf("Virgo");
    }
    if(m == 9 && d >= 23 || m == 10 && d <=22){
        printf("Libra");
    }
    if(m == 10 && d >= 23 || m == 11 && d <= 21){
        printf("Scorpio");
    }
    if(m == 11 && d >= 22 || m == 12 && d <=21){
        printf("Sagittarius");
    }
    return 0;
}
````

(i) The Body Mass Index (BMI) is defined as ratio of the weight of a person (in kilograms) to the square of the height (in meters). Write a program that receives weight and height, calculates the BMI, and reports the BMI category as per the following table:

| BMI CAtegory   | BMI          |
| -------------- | ------------ |
| Starvation     | < 15         |
| Anorexic       | 15.1 to 17.5 |
| Underweight    | 17.6 to 18.5 |
| Ideal          | 18.6 to 24.9 |
| Overweight     | 25 to 29.9   |
| Obese          | 30 to 39.9   |
| Morbidly Obese | >= 40        |

````c
#include<stdio.h>
int main(){
    float bmi, wt, ht;
    printf("Enter weight in kg and height in m : ");
    scanf("%f%f", &wt, &ht);
    bmi = wt / (ht*ht);
    if(bmi < 15){
        printf("Starvation");
    }
    if(bmi > 15 && bmi < 17.6){
        printf("Anorexic");
    }
    if(bmi >= 17.6 && bmi < 18.6){
        printf("Underweight");
    }
    if(bmi >= 18.6 && bmi < 25){
        printf("Ideal");
    }
    if(bmi >= 25 && bmi < 30){
        printf("Overweight");
    }
    if(bmi >= 30 && bmi < 40){
        printf("Obese");
    }
    if(bmi >= 40){
        printf("Morbidly Obese");
    }
    return 0;
}
````

