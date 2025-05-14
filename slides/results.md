<section>

## Application to a wave spectrum

<img src="assets/diagram4.svg" width="600"></img>
</section>


<section>

### Next simplest thing: Apply to JONSWAP spectra

<div style="display: flex; align-items: center; gap: 30px;">
  <div style="flex: 1;">
    <ul>
      <li>Generate JONSWAP spectra</li>
      <li>$U_{10} \in [0, 80]$ m/s</li>
      <li>Fetch = 100 km</li>
    </ul>
  </div>
  <div style="flex: 1; text-align: center;">
    <img src="assets/jonswap_spectra_vs_U10.png" width="400"></img>
  </div>
</div>
</section>


<section>

### Results: Tearing the JONSWAP spectrum

<img src="assets/jonswap_steepness_tear_fraction_2panel.svg" width="800"></img>
</section>

<section>

### Wave spectra with and without tearing

<img src="assets/jonswap_spectra_4panel.png" width="600"></img>
</section>

<section>

### Wave height and MSS with and without tearing

<img src="assets/jonswap_Hs_mss_2panel.svg" width="800"></img>
</section>


<section>

### How about the drag coefficient?

$$
C_D = \frac{\tau}{\rho_a U_{10}^2}
$$

$$
\tau = \tau_{form} + \tau_{skin}
$$

$$
\tau_{form} = \rho_w g \int \frac{S_{in}(f)}{C_p} df
$$

$$
S_{in}(f) = \mathcal{A} \frac{\rho_a}{\rho_w} \left( \frac{U_{\lambda/2} - 1}{C_p} \right)^2 \omega F(f)
$$


</section>


<section>

### Drag coefficient with and without tearing

<img src="assets/fig_cd_tearing.png" width="600"></img>
<div class="fragment">$\Rightarrow$ $C_D$ roll-off exaggerated by occurs at about expected $U_{10}$!</div>

</section>


<section>

### WIP: Waves are not linear when they are steep

<img src="assets/elevation_linear_vs_nonlinear.svg" width="800"></img>

</section>


<section>

### WIP: Aerodynamic drag on the windward side of the wave

<img src="assets/force_linear_vs_nonlinear.svg" width="700"></img>

$\rightarrow$ Drag force is stronger and skewed toward the crest.
</section>