
---
### Problem Statement
1. An executive summary:
* What is your goal?
* Where did you get your data?
* What are your metrics?
* What were your findings?
* What risks/limitations/assumptions affect these findings?
2. Summarize your statistical analysis, including:
* implementation
* evaluation
* inference
3. Clearly document and label each section of your notebook(s)
* Logically organize your information in a persuasive, informative manner.
* Include notebook headers and subheaders, as well as clearly formatted markdown for all written components.
* Include graphs/plots/visualizations with clear labels.
* Comment and explain the purpose of each major section/subsection of your code.
* Document your code for your future self, as if another person needed to replicate your approach.
4. Clearly document all of your decision points in the relevant sections
* How did you acquire your data?
* How did you transform or engineer your data? Why?
* How did you select your model?
* How did you optimize hyperparameters?


---

Best Practices

Organizing your repo
* If you have multiple notebooks, start each filename with a number to assist in organization.
* Give you notebooks descriptive filenames. For example,
    * 1_Scraping.ipynb
    * 2_EDA.ipynb
    * 3_Model_Development.ipynb
* Keep data files in a single folder off the "root" of the repo.
* Keep documentation/reports in a dedicated folder (like data).
* If you have any other resources (images or PDFs), keep them in a dedicated folder (called assets, for example.)
3. Jupyter Notebooks
* Data science is a non-linear, iterative process, but your final notebook should contain a linear "narrative."
* Notebooks should be reproducible, which means that I will get the same results as you did if I clone your repo and run your notebook. Consider the following:
    * Is your data stored in the repo or available via a link?
    * If you use any (ANY) random numbers anywhere, do you have a random seed so that you always get the same result?
    * Is your notebook 100% free of runtime errors?
    * In short, if I open your notebook and click "Cell -> Run All", will your notebook run completely, without errors and give me the same result every time?





* Your presentation should focus on summarizing your problem statement, your approach, your findings, and how it might be used in the future.

* Particularly when presenting to a non-technical audience, remember that what and why can be much more interesting than how:
  * What are you trying to predict?
  * Why are you doing it? Who cares?
  * What are some predictions your model has made? Where they any good?
  * What will you use it for in the future? Are there limitations or risks?
  * Do not use technical terms unless you can clearly and succinctly define them.



---
### Data
The data was obtained from [NASA's API](https://ssd.jpl.nasa.gov/sbdb_query.cgi#x)



[Interactive Orbit Sketch](https://minorplanetcenter.net/db_search/show_orbit?utf8=%E2%9C%93&number=111253&designation=&name=&epoch=2020-05-31.0&peri=6.9239991&m=103.20448&node=310.1588451&incl=42.0283557&e=0.439549138&a=1.7536939&commit=Interactive+Orbit+Sketch)


#### Data Dictionary
[source](https://ssd.jpl.nasa.gov/?glossary&term=phase_a
)  


Name | Description | Data Type  
-----|-------------|----------
`full_name                  ` |   |  `        object`
`neo                        ` |   |  `         int64`
`hazardous                  ` | (PHA) Potentially hazardous asteroid  |  `         int64`
`epoch_cal                  ` |   |  `       float64`
`eccentricity_(e)           ` |An orbital parameter describing the eccentricity of the orbit ellipse. Eccentricity `e` is the ratio of half the distance between the foci `c` to the semi-major axis `a: e=c/a`.   |  `       float64`
`semi_major_axis_(a)        ` |   |  `       float64`
`perihelion_dist_(q)        ` |   |  `       float64`
`inclination_(i)            ` |   |  `       float64`
`perihelion_arg_(w)         ` |   |  `       float64`
`abs_magnitude_(H)          ` |   |  `       float64`
`mean_anomaly               ` |   |  `       float64`
`aphelion_dist_(Q)          ` |   |  `       float64`
`mean_motion_(n)            ` |   |  `       float64`
`min_orbit_intersection_dist` |   |  `       float64`
`t_jupiter                  ` |   |  `       float64`
`asc_node_long_(deg)        ` |   |  `       float64`
`orbital_per_(d)            ` |   |  `       float64`
`orbital_per_(y)            ` |   |  `       float64`
`class                      ` |   |  `        object`
`first_obs                  ` |   |  `datetime64[ns]`
`last_obs                   ` |   |  `datetime64[ns]`
`'diameter_(km)'            ` |   |  `       float64`


The speed at which an asteroid will move is given by

`V = 29.8 km/sec * sqrt( 2/r - 1/a)`

Where r=distance from sun (radius) in astronomical units and a = semi-major axis of the orbit.
If the orbit is circular then a=r and the equation reduces to

`V = 29.8 km/sec * sqrt(1/r)`
`
- Eccentricity: Basically the shape of the ellipse, where values close to zero are more elongated while values closer to one are more circular.
- Semi-major Axis: Half the length of the major axis of the orbit of the asteroid.
- Inclination: The tilt of the orbit from the reference plane. In this case, the reference plane was the ecliptic plane where the orbits of the planets are located.
- Longitude of the Ascending Node: The angle the orbit is rotated from the reference plane's vernal point, basically describes where the asteroid “ascends” out from the reference plane.
- Argument of Periapsis: The orientation of the ellipse, or the angle the orbit is rotated with respect to itself.
- Mean Anomaly: The locations of the asteroid in a certain time period.

---
### Finding Velocity
**The shape of velocity**: [source](https://www.youtube.com/watch?time_continue=728&v=xdIjYBtnvZU&feature=emb_title)
Although we don't know the shape of an orbit, we can find the shape traced out by the velocity vectors. As an asteroid orbits, the velocity changes and rotates tangent to the curve of the orbit (whatever it may look like). We can take the length of the velocity vectors and rotate them so that if we join them at a single point, they form a perfect circle.


---
### Exploratory Data Analysis (EDA)

---
### Modeling

---

### Model Evaluation

---

### Future Steps
---

### Sources
- http://www.columbia.edu/~my2317/asteroidproject.html
- https://www.permanent.com/apollo-amor-aten-near-earth-asteroids.html
- https://ssd.jpl.nasa.gov/sbdb_query.cgi#x
- https://www.quora.com/How-fast-do-asteroids-travel-What-is-the-average-orbital-velocity-of-an-asteroid
- https://en.wikipedia.org/wiki/Orbital_speed
- http://www.asterank.com/3d/
- https://en.wikipedia.org/wiki/Standard_gravitational_parameter
- [Asteroid Image](https://solarsystem.nasa.gov/asteroids-comets-and-meteors/asteroids/16-psyche/in-depth/)
