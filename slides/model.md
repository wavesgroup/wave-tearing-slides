<section>

## A theoretical model for wave tearing by wind
</section>


<section>

## Design principles

To the best of my knowledge, there is no model to predict wave tearing by wind.
The model should then be designed to be, in the first iteration:

1. **Simple** - transparent and from first principles
2. **Useful** - qualitatively predicts observed behavior

If we can accomplish these two goals, we can later pursue more complexity for better accuracy.
</section>


<section>

## 1. Wind blows over a linear (sine) wave that propagates in the same direction

<img src="assets/diagram1.svg" width="800"></img>
</section>



<section>

## 2. Wind blows off the top of the wave crest as spume

<img src="assets/diagram2.svg" width="800"></img>
</section>


<section>

## 3. Wave dissipates by the amount of water removed

<img src="assets/diagram3.svg" width="800"></img>
</section>


<section>

## We seek tear depth $\delta$ as function of wind and wave parameters

<img src="assets/diagram4.svg" width="800"></img>
</section>

<section>

## Tearing criterion

For a water parcel to detach from the crest and break up into
spume, it needs to receive energy from wind.

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

## Aerodynamic forces on a linear wave

<img src="assets/elevation_and_force.svg" width="800"></img>

$C_{Dn} = 1, C_{Dt} = 10^{-3}$
</section>


<section>

### Surface tension energy of spume

$$
E_s = \sigma \Delta A_s
$$

In the simplest approach, assume that all torn volume $V_t$
converts to spume with a uniform radius distribution, _i.e._ $N$ droplets of radius $r$:

$$
E_s = \sigma N 4 \pi r^2
$$

$$
N = \frac{V_t}{\frac{4}{3} \pi r^3}
$$

$$
E_s = \frac{3 \sigma V_t}{r}
$$
</section>


<section>

### Surface tension energy of spume (cont.)

$$
E_s = \frac{3 \sigma V_t}{r}
$$

For a linear wave, $V_t$ can be found analytically as a function of
wave amplitude $a$, wave number $k$, and tearing depth $\delta$:

$$
V_t = \frac{2a}{k} \sqrt{1 - \left(1 - \frac{\delta}{a}\right)^2} - \frac{2(a - \delta)}{k} \cos^{-1}\left(1 - \frac{\delta}{a}\right)
$$

$$
V_t = \frac{\delta}{k} \sqrt{\frac{2 \delta}{a}} + \mathcal{O}\left(\frac{\delta^2}{a^2}\right)
$$

$$
\Rightarrow E_s \propto \frac{\sigma \delta^{\frac{3}{2}}}{a^{\frac{1}{2}} k r}
$$
</section>


<section>

### Tearing criterion (cont.), for small $ak$ and $\delta/a$, and $C_p/U$

$$
\overline{F_d} L_t = E_s
$$

$$
\rho U^2 a \delta \propto \frac{\sigma \delta^{\frac{3}{2}}}{a^{\frac{1}{2}} k r}
$$

$$
\boxed{
\frac{\delta}{a} \propto \left( \frac{\rho U^2 a k r}{\sigma} \right)^2
}
$$
</section>


<section>

## Surface tension energy of spume (cont.)

<img src="assets/surface_tension_energy.svg"></img>
</section>

<section>


## Tearing work and energy

<img src="assets/work_and_energy_linear.svg" width="600"></img>
</section>


<section>

## Tearing work minus energy

<img src="assets/work_minus_energy_linear.svg" width="600"></img>
</section>