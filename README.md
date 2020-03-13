
---
### Problem Statement



---


---
### Data
The data was obtained from [NASA's API](https://ssd.jpl.nasa.gov/sbdb_query.cgi#x)



[Interactive Orbit Sketch](https://minorplanetcenter.net/db_search/show_orbit?utf8=%E2%9C%93&number=111253&designation=&name=&epoch=2020-05-31.0&peri=6.9239991&m=103.20448&node=310.1588451&incl=42.0283557&e=0.439549138&a=1.7536939&commit=Interactive+Orbit+Sketch)


#### Data Dictionary
[source](https://ssd.jpl.nasa.gov/?glossary&term=phase_a
)  


Name | Description | Data Type  
-----|-------------|----------
`neo                        `  | Near-Earth Objects (NEOs) are comets and asteroids that have been nudged by the gravitational attraction of nearby planets into orbits that allow them to enter the Earth’s neighborhood.    |`         int64` |
`hazardous                  `  |  Potentially Hazardous Asteroids (PHAs) are currently defined based on parameters that measure the asteroid's potential to make threatening close approaches to the Earth. Specifically, all asteroids with an Earth Minimum Orbit Intersection Distance (MOID) of 0.05 au or less and an absolute magnitude (H) of 22.0 or less are considered PHAs.  |`         int64` |
`epoch_cal                  `  |     |`       float64` |
`eccentricity_(e)           `  |  Eccentricity e is the ratio of half the distance between the foci c to the semi-major axis `a: e=c/a`. For example, an orbit with e=0 is circular, e=1 is parabolic, and e between 0 and 1 is elliptic.   |`       float64` |
`semi_major_axis_(a)        `  |     |`       float64` |
`perihelion_dist_(q)        `  |     |`       float64` |
`inclination_(i)            `  |   The angle between the vectors normal to the body's orbit plane and the specified reference plane. Typical reference planes are the [ecliptic](https://ssd.jpl.nasa.gov/?glossary&term=ecliptic) plane and the equatorial plane (referred to a specific epoch). |`       float64` |
`perihelion_arg_(w)         `  |     |`       float64` |
`abs_magnitude_(H)          `  |  An asteroid’s absolute magnitude is the visual magnitude an observer would record if the asteroid were placed 1 Astronomical Unit ([au](https://ssd.jpl.nasa.gov/?glossary&term=au)) away, and 1 au from the Sun and at a zero phase angle.   |`       float64` |
`mean_anomaly               `  |  The product of an orbiting body's mean motion and time past [perihelion passage](https://ssd.jpl.nasa.gov/?glossary&term=tp).
   |`       float64` |
`aphelion_dist_(Q)          `  |     |`       float64` |
`mean_motion_(n)            `  |     |`       float64` |
`min_orbit_intersection_dist`  |     |`       float64` |
`t_jupiter                  `  |     |`       float64` |
`asc_node_long_(deg)        `  |  The angle between the reference X-direction (typically the vernal equinox) and the point at which the body passes up (north) through the reference plane. This angle is often denoted as capital omega (Ω).   |`       float64` |
`orbital_per_(y)            `  |  The time required for an object to make a complete revolution along its orbit. For example, the orbital period for a typical main-belt asteroid is about 4 years.   |`       float64` |
`first_obs                  `  |     |`datetime64[ns]` |
`last_obs                   `  |     |`datetime64[ns]` |
`class_APO                  `  |  Earth-crossing NEAs with semi-major axes larger than Earth's (named after asteroid 1862 Apollo).   |`         uint8` |
`class_ATE                  `  |  Earth-crossing NEAs with semi-major axes smaller than Earth's (named after asteroid 2062 Aten).   |`         uint8` |
`class_IEO                  `  |  NEAs whose orbits are contained entirely with the orbit of the Earth (named after asteroid 163693 Atira).   |`         uint8` |
`stand_grav_param           `  |     |`       float64` |
`rel_velocity_Q             `  |     |`       float64` |
`rel_velocity_q             `  |     |`       float64` |

**Data Dictionary Sources**  
[NASA Center for Near Earth Object Glossary](https://cneos.jpl.nasa.gov/glossary/h.html)  
[NASA Solar System Dynamics Glossary](https://ssd.jpl.nasa.gov/?glossary&term=H)

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
- [PHA Orbits](https://solarsystem.nasa.gov/resources/405/orbits-of-potentially-hazardous-asteroids-phas/?category=planets_jupiter)
- [Asteroid 2002 AJ129](https://www.nasa.gov/feature/jpl/asteroid-2002-aj129-to-fly-safely-past-earth-february-4)
- [Geometry of Elliptical Orbit](http://astrolab.phys.utk.edu/Lindsay_manual/orbit_of_mercury/lab_orbit_of_mercury_v02.pdf)
