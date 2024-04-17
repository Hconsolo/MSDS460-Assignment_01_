<a name="readme-top"></a>

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![LinkedIn][linkedin-shield]][linkedin-url]


<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Hconsolo/MSDS460-Assignment_01_">
    <img src="002. Pictures Paper/Northwestern_Wildcats_logo.svg" alt="Logo" width="80" height="80">
  </a>
  <h3 align="center">Northwestern University</h3>
  <h3 align="center">MSDS 460-DL : Decision Analytics</h3>
  <h3 align="center">ASSIGNMENT 1: Linear Programming Example</h3>
  <h4 align="center">The Diet Problem Revisited (Spring 2024)</h4>
  <h4 align="center">April 16, 2023</h4>
  <h4 align="center">Humberto Consolo Holanda</h4>

</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#Contact">Contact</a></li>
    <li><a href="#Introduction">Introduction</a></li>
    <li><a href="#Method">Method</a></li>
    <li><a href="#Results">Results</a></li>
    <li><a href="#Conclusion">Conclusion</a></li>
    <li><a href="#Reference">Reference</a></li>
  </ol>
</details>

<!-- CONTACT -->
## Contact

Humberto Consolo Holanda - [https://www.linkedin.com/in/hconsolo](https://www.linkedin.com/in/hconsolo) - humbertoconsoloholanda2025@u.northwestern.edu

Project Link: [https://github.com/Hconsolo/MSDS460-Assignment_01_](https://github.com/Hconsolo/MSDS460-Assignment_01_)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ABOUT THE PROJECT -->
## Introduction

[![Product Name Screen Shot][product-screenshot]](https://canvas.northwestern.edu/)

In this assignment, we will be discussing the use of linear programming to solve the Stigler diet problem, with the help of Python (Dantzig 1990). The problem aims to find a diet that meets specific nutritional requirements while minimizing the cost. We can achieve this by optimizing a linear objective function with linear constraints, which will give us the optimal combination of food items that meet our requirements at the lowest possible cost.

We have used food prices for six meals and considered eight nutritional requirements to solve this problem. Our primary focus was to find the minimum-cost diet that would fulfill the necessary nutrients. In our research, we paid special attention to four specific nutrients: Vitamin D, Calcium, Iron, and Potassium. We did not include Sodium, Protein, and Energy in our study because these nutrients are commonly found in packaged foods or meat, poultry, and fish, which are good sources of protein. By excluding them, we were able to narrow down our research and make more informed decisions about our diet.

Table 01 lists the constraints for each nutrient. We have also included a list of items that are good sources of essential nutrients according to the Dietary Guidelines for Americans (2024). The goal is that if any constraint cannot be quickly met with the proposed meals, we can add another item to provide the missing nutrient.

| Component   | Max/Min   | Daily Amount and measure            | Important Food items                 |
|:------------|:----------|:------------------------------------|:-------------------------------------|
| Sodium      | Maximum   | 5,000 milligrams (mg)               | Not applicable                       |
| Energy      | Minimum   | 2,000 Calories (kilocalories, kcal) | Not applicable                       |
| Protein     | Minimum   | 50 grams (g)                        | Not applicable                       |
| Vitamin D   | Minimum   | 20 micrograms (mcg)                 | Salmon, Milk, Soy Beverage           |
| Calcium     | Minimum   | 1,300 milligrams (mg)               | Yogurt, Milk, Tofu                   |
| Iron        | Minimum   | 18 milligrams (mg)                  | Spinach, Ready-to-eat cereal, Oyster |
| Potassium   | Minimum   | 4,700 milligrams (mg)               | Yogurt, Milk, Fish                   |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Method

For this task, we employed Python and the following third part libraries to help with basic data handling tasks and to solve the the LP problem.

* Pandas - Data Wrangling and Processing
* Matplotlib & Seaborn - Data Visualization
* PulP - Provides a modeling framework and LP optimization tool

We have collected information on the nutritional value of five meals that are easily available online. These meals are Kraft Mac & Cheese, Amy's Thai Pad Thai, Fresh Express Chopped Caesar Salad Kit, Spinach Scramble, Salmon, Rice, and Broccoli. To ensure that all the necessary nutrients are covered, we have also included milk as a sixth meal option to be consumed during the day, since it is cheap and provides calcium, vitamin D, and potassium (Dietary Guidelines for Americans 2020). We chose pre-packaged and easy-to-prepare meals that require no more than five ingredients or have ingredients readily available in the package. We obtained the prices and nutritional information from Mariano's website (2024), and Table 02 summarizes this information along with the pre-packaged meal prices or the pro-rated cost per meal. The prices do not include any costs associated with food preparation, such as utility costs or labor. For the recipes that required preparation, we calculate the prorated costs and nutritional content based on the key ingredients based on the recipes from online websites. On the repository of this assignment one can find the nutritional values on a table, files containing the nutrition information and prices from Mariano’s website.

#### Table 02: Nutrition facts and prices for the meal options.

| Food Item (meal)                       |   Price ($) |   Energy (calories) |   Sodium (mg) |   Protein (g) |   Vitamin D (mcg) |   Calcium (mg) |   Iron (mg) |   Potassium (mg) |
|:---------------------------------------|------------:|--------------------:|--------------:|--------------:|------------------:|---------------:|------------:|-----------------:|
| Kraft Mac & Cheese                     |        0.46 |              250    |        560    |          9    |               0   |         110    |        2.5  |           330    |
| Amy's Thai Pad Thai                    |        6.79 |              410    |        760    |         12    |               0   |          90    |        3.9  |           360    |
| Fresh Express Chopped Caesar Salad Kit |        1.8  |              160    |        310    |          3    |               0   |          90    |        0.9  |           190    |
| Spinach Scramble                       |        1.16 |              161.67 |        458.17 |         13.08 |               2   |          86.68 |        2.65 |           351.42 |
| Salmon, Rice, and Broccolis            |        3.83 |              322.5  |        549.25 |         27.5  |              12.3 |          40.75 |        1.15 |           618.5  |
| Fat Free Skim Milk                     |        0.46 |               80    |        120    |          8    |             100   |         300    |        0    |           390    |


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Results

#### Table 03: Optimal weekly portion for each food item (meal).

| Food Item (meal)                       |   Model 01 |   Model 02 |   Model 03 |
|:---------------------------------------|-----------:|-----------:|-----------:|
| Amy's_Thai_Pad_Thai                    |        0   |        1   |        1   |
| Fat_Free_Skim_Milk                     |       41.7 |       40.7 |       28   |
| Fresh_Express_Chopped_Caesar_Salad_Kit |        0   |        1   |        1   |
| Kraft_Mac_&_Cheese                     |       50.4 |       47   |       27.9 |
| Salmon,_Rice,_and_Broccolis            |        0   |        1   |        3.9 |
| Spinach_Scramble                       |        0   |        1   |       28   |

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Reference

1. [Camarena, Omar Antolín. "Standard form for Linear Programs." Instituto de Matemáticas, UNAM. Accessed on April 16, 2024](https://www.matem.unam.mx/~omar/math340/std-form.html)
2. [Dantzig, George B. 1990. “The Diet Problem.” Informs. 20:4, 43–47](https://www.mpi-inf.mpg.de/fileadmin/inf/d1/teaching/winter18/Ideen/Materialien/Dantzig-Diet.pdf)
3. [U.S. Department of Agriculture and U.S. Department of Health and Human Services. Dietary Guidelines for Americans, 2020-2025. 9th Edition. December 2020. Available at DietaryGuidelines.gov.](https://www.dietaryguidelines.gov/resources/2020-2025-dietary-guidelines-online-materials)


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/hconsolo
[product-screenshot]: https://upload.wikimedia.org/wikipedia/commons/7/7c/Northwestern_Wildcats_logo.svg