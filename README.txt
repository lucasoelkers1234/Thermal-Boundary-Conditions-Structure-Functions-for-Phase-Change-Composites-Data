Measured transient thermal impedance Zth(t) for the article
"Thermal Boundary Conditions and the Limits of Cumulative Structure Functions for Phase Change Composites"
L. H. Oelkers, R. C. McAfee, M. C. Fish, P. J. Shamberger (submitted to IEEE Trans. Compon., Packag., Manuf. Technol.)

Sample: hexadecane-filled micro-skived copper heat spreader (phase change composite), melting temperature 17.3 C.

CONTENTS
  ColdSideTemperature_series/  cold side temperature Tf varied from 3.4 to 20.1 C at q'' = 4.25 W/cm2
      heating/   15 conditions + purely sensible reference (Tf = 25.0 C)
      cooling/   15 conditions + purely sensible reference (Tf = 25.0 C)
      reference_members/   the two records (up0925, up0925v2) whose mean is the Tf = 25.0 C reference
  HeatFlux_series/             heat flux q'' varied from 0.425 to 4.25 W/cm2 at Tf = 17.1 C
      heating/   10 conditions + purely sensible reference (Tf = 25.0 C, q'' = 4.25 W/cm2)
      cooling/   10 conditions + purely sensible reference (Tf = 25.0 C, q'' = 4.25 W/cm2)
  conditions.csv   one row per file: series, mode, Tf and q'' (label and measured), heater power, the reference
                   used for that file, acquisition date, record tag, number of samples, time range, final Zth,
                   and the original file name.

FILE FORMAT
  CSV, one header row: time_s, Zth_K_per_W.
  time_s       time since the start of the heating step (heating) or since its end, t' (cooling), s.
  Zth_K_per_W  thermal impedance, K/W (= C/W).
  Sampling interval 20.48 ms. Only samples at t > 0 are included; these are all samples used in the analysis.
  Values are copied unchanged from the analysis input files.

DEFINITIONS (Methods of the article)
  Heating:  Zth(t) = [Th(t) - Th,0] / P, during a 3,500 s power step; Th,0 is the hot side temperature at t = 0.
  Cooling:  Zth(t') = [Th(tp) - Th(tp + t')] / P, where tp is the end of the step and t' the elapsed cooling time;
            the heating value of P is retained. Cooling records are 271 to 4,500 s long.
  Th is the hot side (heater) temperature and P the heater power (conditions.csv, power_W).
  Each series has its own purely sensible reference, measured at Tf = 25.0 C and q'' = 4.25 W/cm2 in the same
  assembly. The PCC stack was reassembled between the two series. The cold side temperature reference is the mean of
  two records (reference_members/) on the time grid of the first, over their common time range; the largest
  difference between a member and the mean is 0.0055 K/W (heating) and 0.0027 K/W (cooling).
  Thermal impedance suppression: dZth(t) = Zth,ref(t) - Zth(t), over the time range measured in both records.
