<section>

## A criterion for wave tearing by wind
</section>


<section>

## Design principles

To the best of my knowledge, there is no model to predict wave tearing by wind.
The model should then be designed to be, in the first iteration:

1. **Simple** - transparent and from first principles
2. **Useful** - qualitatively predicts observed behavior

If we can first accomplish these two goals, we can later pursue more complexity for higher accuracy.
</section>


<section>

## 1. Wind blows over a wave that propagates in the same direction

<img src="assets/diagram1.svg" width="800"></img>
</section>



<section>

## 2. Wind tears the top of the wave crest off, creating spume

<img src="assets/diagram2.svg" width="800"></img>
</section>


<section>

## 3. Wave energy dissipates corresponding to the amount of water lost

<img src="assets/diagram3.svg" width="800"></img>
</section>


<section>

## We seek tear depth $\delta$ as function of wind and wave parameters

<img src="assets/diagram4.svg" width="800"></img>
</section>

<section>

## Tearing criterion

For a water parcel to detach from the crest and break up into
spume, it needs to receive energy from the wind.

The wind does work on a sloped wave surface via aerodynamic drag.

The mechanical energy from wind is transferred entirely
into surface tension energy that holds all spume droplets.

$$
W_t = E_s
$$

where $W_t$ is the tearing work by wind and $E_s$ is the surface tension energy of spume produced by the tear.
</section>


<section>

## Tearing criterion (cont.)

$$
W_t = E_s
$$

$$
\overline{F_d} L_t = \sigma \Delta A_s 
$$

where:

* $\overline{F_d}$: area-integrated aerodynamic drag force by the wind
* $L_t$: tear path ($\propto 1/k$)
* $\sigma$: surface tension of water
* $\Delta A_s$: change in total surface area of the water parcel
</section>


<section>

### Aerodynamic drag by the wind

<div style="font-size: 0.8em;">
Consider normal (pressure) and tangential (shear stress) components:

$$
\overline{F_d} = \int_{a-\delta}^{a} \left[F_{dn}(z) + F_{dt}(z)\right] dz
$$

Use aerodynamic drag formula to parameterize force as function of mean velocity:

$$
F_{dn}(z) = \frac{1}{2} \rho C_{Dn} (U - Cp)^2 \sin\alpha(z)
$$

$$
F_{dt}(z) = \frac{1}{2} \rho C_{Dt} (U - Cp)^2 \cos{\alpha(z)}
$$

* $U$: wind speed at crest height
* $C_p$: wave phase speed
* $\alpha = \tan^{-1}\left(\frac{\partial \eta}{\partial x}\right)$: local wave slope
* $C_{Dn}$ and $C_{Dt}$: drag coefficients (tunable)

</div>
</section>


<section>

### Aerodynamic forces on a linear wave

<img src="assets/elevation_and_force.svg" width="800"></img>

$C_{Dn} = 1, C_{Dt} = 10^{-3}$
</section>


<section>

### Surface tension energy of spume

$$
E_s = \sigma \Delta A_s
$$

Surface tension energy of spume is proportional to its volume
divided by the effective droplet radius $r$:

$$
E_s = \sigma N 4 \pi r^2
$$

$$
N = \frac{V_t}{\frac{4}{3} \pi r^3}
$$

$$
\Rightarrow E_s = \frac{3 \sigma V_t}{r}
$$
</section>


<section>

### Surface tension energy of spume (cont.)

$$
E_s = \frac{3 \sigma V_t}{r}
$$

For a linear wave, $V_t$ can be found analytically as a function of
wave amplitude $a$, wavenumber $k$, and tear depth $\delta$:

$$
V_t = \frac{\delta}{k} \sqrt{\frac{2 \delta}{a}} + \mathcal{O}\left(\frac{\delta^2}{a^2}\right)
$$

$$
\Rightarrow E_s = \frac{3 \sigma \delta}{kr} \sqrt{\frac{2\delta}{a}}
$$
</section>


<section>

### Tearing criterion (cont.), for small $ak$

$$
\overline{F_d} L_t = E_s
$$

where

$$
F_d = \frac{1}{2} \rho C_D U_c^2 ak\ \delta
$$

$$
L_t = \frac{\lambda}{2} = \frac{\pi}{k}
$$


$$
E_s = \frac{3\sigma \delta}{kr} \sqrt{\frac{2\delta}{a}} 
$$
</section>

<section>

### Tearing criterion (cont.), for small $ak$

$$
\boxed{
\frac{\delta}{a} = \left(\frac{\pi}{6} \frac{\rho C_D U_c^2 a k r}{\sigma} \right)^2
}
$$

$\Rightarrow$ tear fraction is quadratic in wave steepness and quartic in wind speed.

Spume droplet radius $r$ yet to be determined.
</section>


<section>

### Spume radius distribution based on Veron et al. (2012)

<div style="display: flex; justify-content: space-between;">
  
  <div style="flex: 1;">
    <img src="assets/spume_spectrum_veron2012.svg" width="450">
  </div>
  
  <div style="flex: 1;">
    <img src="assets/Veron_etal_2012_GRL_Fig04c.png" width="450">
    <a href="https://doi.org/10.1029/2012GL052603">Veron et al. (2012, GRL)</a>
  </div>

</div>


$$
\Rightarrow r_{eff} = \frac{3 \int{V(r) dr}}{\int{A(r) dr}}
$$

</section>


<section>

### Tear fraction $\delta/a$ for wind over monochromatic wave train

<img src="assets/tear_fraction_analytical.svg" width="600"></img>
</section>