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
  <a href="https://upload.wikimedia.org/wikipedia/commons/7/7c/Northwestern_Wildcats_logo.svg">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">ASSIGNMENT 1: Linear Programming Example - The Diet Problem Revisited (Spring 2024)</h3>

</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- CONTACT -->
## Contact

Humberto Consolo Holanda - [https://www.linkedin.com/in/hconsolo](https://www.linkedin.com/in/hconsolo) - humbertoconsoloholanda2025@u.northwestern.edu

Project Link: [https://github.com/Hconsolo/MSDS460-Assignment_01_](https://github.com/Hconsolo/MSDS460-Assignment_01_)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ABOUT THE PROJECT -->
## Introduction

[![Product Name Screen Shot][product-screenshot]](https://example.com)

In this assignment, we will be discussing the use of linear programming to solve the Stigler diet problem, with the help of Python. The problem aims to find a diet that meets specific nutritional requirements while minimizing the cost. We can achieve this by optimizing a linear objective function with linear constraints, which will give us the optimal combination of food items that meet our requirements at the lowest possible cost.

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

### Libraries

For this week’s assignment, our exercise applied linear programming (LP) to the diet problem. This problem aims to find the minimum-cost diet based on the price of the food serving for six meals to achieve the eight nutritional requirements based on Sodium, Energy, Protein, Vitamin D	Calcium, Iron, and Potassium.

* Pandas - Data Wrangling and Processing
* Matplotlib - Data Visualization
* Seaborn - Data Visualization
* PulP - Provides a modeling framework and LP optimization tool

| Component   | Max/Min   | Daily Amount and measure            |
|:------------|:----------|:------------------------------------|
| Sodium      | Maximum   | 5,000 milligrams (mg)               |
| Energy      | Minimum   | 2,000 Calories (kilocalories, kcal) |
| Protein     | Minimum   | 50 grams (g)                        |
| Vitamin D   | Minimum   | 20 micrograms (mcg)                 |
| Calcium     | Minimum   | 1,300 milligrams (mg)               |
| Iron        | Minimum   | 18 milligrams (mg)                  |
| Potassium   | Minimum   | 4,700 milligrams (mg)               |

<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* [![Next][Next.js]][Next-url]
* [![React][React.js]][React-url]
* [![Vue][Vue.js]][Vue-url]
* [![Angular][Angular.io]][Angular-url]
* [![Svelte][Svelte.dev]][Svelte-url]
* [![Laravel][Laravel.com]][Laravel-url]
* [![Bootstrap][Bootstrap.com]][Bootstrap-url]
* [![JQuery][JQuery.com]][JQuery-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

_Below is an example of how you can instruct your audience on installing and setting up your app. This template doesn't rely on any external dependencies or services._

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Method

For this task, we employed Python and the following third part libraries to help with basic data handling tasks and to solve the the LP problem.

* Pandas - Data Wrangling and Processing
* Matplotlib & Seaborn - Data Visualization
* PulP - Provides a modeling framework and LP optimization tool

We have collected information on the nutritional value of five meals that are easily available online. These meals are Kraft Mac & Cheese, Amy's Thai Pad Thai, Fresh Express Chopped Caesar Salad Kit, Spinach Scramble, Salmon, Rice, and Broccoli. To ensure that all the necessary nutrients are covered, we have also included milk as a sixth meal option to be consumed during the day, since it is cheap and provides calcium, vitamin D, and potassium (Dietary Guidelines for Americans 2024). We chose pre-packaged and easy-to-prepare meals that require no more than five ingredients or have ingredients readily available in the package. We obtained the prices and nutritional information from Mariano's website (2024), and Table 02 summarizes this information along with the pre-packaged meal prices or the pro-rated cost per meal. The prices do not include any costs associated with food preparation, such as utility costs or labor. For the recipes that required preparation, we calculate the prorated costs and nutritional content based on the key ingredients based on the recipes from online websites. On the repository of this assignment one can find the nutritional values on a table, files containing the nutrition information and prices from Mariano’s website. 

#### Table 02: Nutrition facts and prices for the meal options.

| Food Item                              |   Price ($) |   Energy (calories) |   Sodium (mg) |   Protein (g) |   Vitamin D (mcg) |   Calcium (mg) |   Iron (mg) |   Potassium (mg) |
|:---------------------------------------|------------:|--------------------:|--------------:|--------------:|------------------:|---------------:|------------:|-----------------:|
| Kraft Mac & Cheese                     |        0.46 |              250    |        560    |          9    |               0   |         110    |        2.5  |           330    |
| Amy's Thai Pad Thai                    |        6.79 |              410    |        760    |         12    |               0   |          90    |        3.9  |           360    |
| Fresh Express Chopped Caesar Salad Kit |        1.8  |              160    |        310    |          3    |               0   |          90    |        0.9  |           190    |
| Spinach Scramble                       |        1.16 |              161.67 |        458.17 |         13.08 |               2   |          86.68 |        2.65 |           351.42 |
| Salmon, Rice, and Broccolis            |        3.83 |              322.5  |        549.25 |         27.5  |              12.3 |          40.75 |        1.15 |           618.5  |
| Fat Free Skim Milk                     |        0.46 |               80    |        120    |          8    |             100   |         300    |        0    |           390    |


Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Results

#### Table 02: Nutrition facts and prices for the meal options.

| Food Item                              |   Model 01 |   Model 02 |   Model 03 |
|:---------------------------------------|-----------:|-----------:|-----------:|
| Amy's_Thai_Pad_Thai                    |        0   |        1   |        1   |
| Fat_Free_Skim_Milk                     |       41.7 |       40.7 |       28   |
| Fresh_Express_Chopped_Caesar_Salad_Kit |        0   |        1   |        1   |
| Kraft_Mac_&_Cheese                     |       50.4 |       47   |       27.9 |
| Salmon,_Rice,_and_Broccolis            |        0   |        1   |        3.9 |
| Spinach_Scramble                       |        0   |        1   |       28   |


<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- ACKNOWLEDGMENTS -->
## Reference

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

1. [Camarena, Omar Antolín. "Standard form for Linear Programs." Instituto de Matemáticas, UNAM. Accessed on April 16, 2024](https://www.matem.unam.mx/~omar/math340/std-form.html)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/hconsolo
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
