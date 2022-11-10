# Econometrics Cheat Sheet Project

Econometrics cheat sheet created using $\LaTeX$ with a summarized review of:

* **Basic econometrics concepts**: econometrics definitions, data type, phases of a model, regression and correlation analysis.
* **Assumptions and properties** of the linear regression model.
* **Ordinary Least Squares** (OLS) equations, coefficient interpretatation, error measures, r-squared.
* **Hypothesis testing and confidence intervals**.
* **Dummy variables and structural change**.
* **Predictions**.
* **Popular OLS problems** (multicollinearity, heteroscedasticity and auto-correlation): consequences, detection and correction.
* **Time series** analysis and peculiarities.

:bulb: Opinions, ideas and collaboration proposals are heard through GitHub or by email (marcelomijas@gmail.com). Also, my [LinkedIn](https://www.linkedin.com/in/marcelomorenop/).

### Download links

**Econometrics Cheat Sheet**. Current version: `2.7` (last updated 22 oct. 2022)

|              | PDF file                                                          | TeX file                                                          |
| :----------: | :---------------------------------------------------------------: | :---------------------------------------------------------------: |
| English :uk: | [en.pdf](econometrics-cheatsheet/econometrics-cheatsheet-en.pdf)  | [en.tex](econometrics-cheatsheet/econometrics-cheatsheet-en.tex)  |
| Spanish :es: | [es.pdf](econometrics-cheatsheet/econometrics-cheatsheet-es.pdf)  | [es.tex](econometrics-cheatsheet/econometrics-cheatsheet-es.tex)  |

**Time Series Cheat Sheet**. Current version: `ts1.1` (last updated 5 oct. 2022)

|              | PDF file                                                        | TeX file                                                        |
| :----------: | :-------------------------------------------------------------: | :-------------------------------------------------------------: |
| English :uk: | [en.pdf](time-series-cheatsheet/time-series-cheatsheet-en.pdf)  | [en.tex](time-series-cheatsheet/time-series-cheatsheet-en.tex)  |
| Spanish :es: | [es.pdf](time-series-cheatsheet/time-series-cheatsheet-es.pdf)  | [es.tex](time-series-cheatsheet/time-series-cheatsheet-es.tex)  |

## Roadmap

- [x] Release of pages 1 and 2 of `econometrics-cheatsheet` covering basic concepts, assumptions and properties, OLS equations, and more.

- [x] Release of page 3 of `econometrics-cheatsheet` covering popular OLS problems.

- [x] Release of an Spanish version of `econometrics-cheatsheet`.

- [x] Release of a cheat sheet exclusively dedicated to time series in the context of econometrics, `time-series-cheatsheet`.

- [x] Release of an Spanish version of `time-series-cheatsheet`.

- [ ] Release of a cheat sheet with more common problems in econometrics and additional models (VAR, VECM, ...), `additional-cheatsheet`.
  - :warning: :construction: A work in progress can be found at [add-en.pdf](additional-cheatsheet/additional-cheatsheet-en.pdf)

- [ ] Styled version of the cheat sheets (background colors, styled sections, more appealing plots, etc.)

## Frequently Asked Questions (FAQ)

### What does $\mathrm{residualized}$ $x_j$ means?

Those are the residuals from a OLS regression between $x_j$ and all the other $x$ 's. Error measures and r-squared can also be obtained from this regression.

### Why is $\beta_0$ the constant term? My reference manual / professor's definition of the econometric model is different.

There is some debate about the correct way to name the coefficients, the sub-index of the coefficients and sub-index of the variables of a model. This could have an impact on how some statistics like the adjusted R-squared or some tests like the F contrast formulas are written.

For example, while some econometricians write the multiple regression model with a constant term like this:

$$y_i = \beta_0 + \beta_1 x_{1i} + \beta_2 x_{2i} + ... + \beta_k x_{ki} + u_i \rightarrow \mathrm{Specification (1)}$$

There are others that refer to that same econometric model as:

$$y_i = \beta_1 + \beta_2 x_{2i} + \beta_3 x_{3i} + ... + \beta_k x_{ki} + u_i \rightarrow \mathrm{Specification (2)}$$

Others:

$$y_i = \alpha + \beta_1 x_{1i} + \beta_2 x_{2i}  + ... + \beta_k x_{ki} + u_i \rightarrow \mathrm{Specification (3)}$$

All the above are equally valid representations of the multiple regression model. In the specification $(1)$, $\beta_0$ represents the constant term, while in specification $(2)$ and $(3)$ it is represented by $\beta_1$ and $\alpha$, respectively.

In this project, the specification used is the first $(1)$, so we can say that there are $k$ independent variables and $k+1$ coefficients (including the constant term), the same could be said for the specification $(3)$. There are no difference in the statistics and tests formula definition between this two specifications, $k_{(1)} = k_{(3)}$.

The same cannot be said about specification $(2)$, because there is a difference between it and the rest: $k_{(1)} = k_{(3)} \neq k_{(2)}$. But there is a relation between the three, $k_{(2)} = k_{(1)}-1$ (also considering $k_{(1)} = k_{(3)}$). This way, a "translation" between formulas for different representations is possible. For example, the adjusted R-squared:

$$\mathrm{Specification (1)(3)} \rightarrow \overline{R}^2 = 1 - \frac{n-1}{n-k-1} (1-R^2)$$

$$\mathrm{Specification (2)} \rightarrow \overline{R}^2 = 1 - \frac{n-1}{n-k} (1-R^2)$$

### Where is the non matrix version of the standard error of the $\hat{\beta}$ 's?

For space reasons, the version included in the cheatsheet is the matricial one. It is perfectly valid and equal to the non matrix version.

The non matrix version:

$$\mathrm{se}(\hat{\beta}_j)=\sqrt{\frac{\hat{\sigma}^2}{SST_j(1-R^2_j)}},j=1,...,k$$

## Resources

In addition to the notes taken from the [Degree in Economics by the King Juan Carlos University](https://www.urjc.es/universidad/calidad/560-economia) and the [Master in Applied Statistics by Máxima Formación and Nebrija University](https://www.maximaformacion.es/masters/master-de-estadistica-aplicada-con-r-software/), the books used:

[1] Baltagi, B. H. (2011). *Econometrics*. New York: springer.

[2] Gujarati, D. N., Porter, D. C., & Gunasekar, S. (2012). *Basic econometrics*. Tata McGraw-Hill Education.

[3] James, G., Witten, D., Hastie, T., & Tibshirani, R. (2013). *An introduction to statistical learning*. New York: springer.

[4] Lütkepohl, H., & Krätzig, M. (Eds.). (2004). *Applied Time Series Econometrics*. Cambridge: Cambridge University Press.

[5] Ruiz-Maya, L., & Pliego, F. J. M. (2004). *Fundamentos de inferencia estadística*. AC.

[6] Stock, J. H., & Watson, M. W. (2012). *Introduction to econometrics*. New York: Pearson.

[7] Wooldridge, J. M. (2015). *Introductory econometrics: A modern approach*. Cengage learning.

## Contributions

* Reddit user \_bheg_ - Pointed out about the importance of including strong and weak exogeneity and their consequences on bias and consistency properties of OLS.

## Support the project

The first (and I think, **the best**) way to help the project is to **directly support the authors of the manuals that are included in the resources section** (for example, by buying their works). Each and every one of the authors of the manuals are wonderful minds who have contributed a lot to econometrics and statistics. 

Another great way to support the project is by sharing it and :star: it!
