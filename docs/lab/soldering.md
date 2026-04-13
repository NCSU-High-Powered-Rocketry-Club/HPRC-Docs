# Soldering

Soldering is the process of joining two or more electronic components together by melting a [filler metal](#solder) to create a strong electrical and mechanical bond.

This guide will cover the basics of soldering, including the tools and materials needed, the steps to soldering, some tips for achieving good results, and of course safety precautions.

## Tools and Materials

There are several tools and materials that you will need for soldering. Here are some of the most common ones:

### Solder

Solder is a metal alloy, often made of tin and optionally, lead. It comes in the form of a thin wire or a paste and is used to create a strong bond between electronic components.

Here are 3 types of solder we have in the lab:

<div class="grid cards" markdown>

-   ![Unleaded 0.3 mm](pictures/soldering/unleaded_solder_0.3mm.jpg){ width="70%" loading="lazy" }

    **Unleaded 0.3 mm**  
    Fine pitch work, high melting point

-   ![Leaded 0.8 mm](pictures/soldering/leaded_solder_0.8mm.jpg){ width="70%" loading="lazy" }

    **Leaded 0.8 mm**  
    Easier flow, stronger joints

-   ![Solder paste](pictures/soldering/solder_paste.jpg){ width="70%" loading="lazy" }

    **Solder paste**  
    For sensitive SMD components, requires a reflow oven or hot air rework station

</div>

When should you use what solder? It depends on the application. 

For fine pitch work, such as soldering small SMD components, a thinner solder (like 0.3 mm) is often preferred for better control and precision.

For general-purpose soldering, a thicker solder (like 0.8 mm) can be easier to work with and provides stronger joints. 

Solder paste is typically used for surface mount devices (SMDs) and requires specialized equipment for reflow soldering, such as a [reflow oven]() or a [hot air rework station](#hot-air-rework-station).

The choice between leaded and unleaded solder depends on personal preference. It is much easier to work with leaded solder since it has a lower melting point and better flow characteristics. 

!!! warning "Lead Safety"
    Leaded solder contains lead, which is toxic. Always **wash** your hands after handling leaded solder, since there are fine particulates that can settle on your fingers. Always use a [fume extractor](#fume-extractor) when soldering to avoid inhaling flux fumes.

### Soldering Iron

A soldering iron is a handheld tool that heats up to melt [solder](#solder). It typically has a pointed tip that allows for precise application of heat to the components being soldered.

We have 2 good soldering irons in the lab:

<div class="grid cards" markdown>

-  ![TC 22 Soldering Station](pictures/soldering/TC22_soldering_station.jpg){ width="70%" loading="lazy" }

    **TC 22 Soldering Station**  
    Digital display, extremely fast heat up time, needs a power outlet

- ![Pinecil soldering station](pictures/soldering/pinecil_soldering_iron.jpg){ width="70%" loading="lazy" }

    **Pinecil Soldering Station**  
    Compact, portable, and USB-C powered (needs a good 35W+ PD cable).

</div>

### Flux

Flux is a chemical agent that helps to clean, remove oxides, promotes wetting, and improves the flow of [solder](#solder) and the quality of the joint. It can come in various forms, such as liquid, paste, or as a core in solder wire.

We have 2 types of flux in the lab:

<div class="grid cards" markdown>
-  ![Flux pen](pictures/soldering/flux_pen.jpg){ width="70%" loading="lazy" }

    **Flux Pen**  
    Depress the tip to release flux, needs cleaning after soldering
  
- ![No-Clean Flux](pictures/soldering/no_clean_flux.jpg){ width="70%" loading="lazy" }

    **No-Clean Flux**  
    Suitable for general use, does not require cleaning after soldering.
</div>


### Solder Wick

Solder wick, also known as desoldering braid, is a braided copper wire that is used to remove excess [solder](#solder) from a joint. It works by absorbing the molten solder when heated with a [soldering iron](#soldering-iron).

<div class="grid cards" markdown>
-  ![Solder Wick](pictures/soldering/solder_wick.jpg){ width="60%" loading="lazy" }

    **Solder Wick**  
    The copper braid absorbs molten solder
</div>


### Solder Sucker

A solder sucker, also known as a desoldering pump, is a handheld tool that creates suction to remove molten [solder](#solder) from a joint. It typically consists of a plunger and a nozzle that can be placed over the molten solder to be removed.

<div class="grid cards" markdown>
-  ![Solder Sucker](pictures/soldering/solder_sucker.jpg){ width="70%" loading="lazy" }

    **Solder Sucker**  
    Press down the red push head of the plunger to create suction, place the nozzle over molten solder, and hit the release button to suck up the solder.

-  ![Old Solder Sucker](pictures/soldering/old_solder_sucker.jpg){ width="70%" loading="lazy" }

    **Old Solder Sucker**  
    A more traditional design - can be less effective since the suction isn't as strong.
</div>

### Fume Extractor

This is a simple centrifugal fan which when turned on, creates negative pressure to pull in the fumes generated during soldering. There is an activated carbon filter inside the fume extractor which adsorbs the fumes before releasing the air back into the environment.

<div class="grid cards" markdown>
-  ![Fume Extractor](pictures/soldering/fume_extractor.jpg){ width="50%" loading="lazy" }

    **Fume Extractor**  
    Simply turn it on and place it near your soldering work to capture the fumes.
</div>


### Tip Tinner

Tip tinner is a maintenance product for soldering iron tips. It typically contains flux and a sacrificial [solder](#solder)/metal compound that helps remove oxides and restores the plated surface of a tip.

This is only used as a last resort if your soldering iron tip is oxidized and not wetting properly. Should be used sparingly.

<div class="grid cards" markdown>
-  ![Tip Tinner](pictures/soldering/tip_tinner.jpg){ width="40%" loading="lazy" }

    **Tip Tinner**  
    Simply heat the soldering iron tip and dip it into the tip tinner compound.
</div>

### Kapton Tape

Kapton tape is a polyimide film tape with excellent heat resistance and electrical insulation properties.

You apply the tape in areas of a PCB you don't want heated from a [soldering iron](#soldering-iron) or [hot air rework station](#hot-air-rework-station). Our tape is rated for 250°C.

<div class="grid cards" markdown>
-  ![Kapton Tape](pictures/soldering/kapton_tape.jpg){ width="50%" loading="lazy" }

    **Kapton Tape**  
    High-temperature insulating tape commonly used in SMD work.

-  ![Kapton Tape on FIRM](pictures/soldering/kapton_tape_on_firm.jpg){ width="40%" loading="lazy" }

    **Kapton Tape on FIRM**  
    Real world use of kapton tape while reworking on a [FIRM]().
</div>


### Hot Air Rework Station

A hot air rework station uses a heated stream of air to melt [solder](#solder), allowing removal and replacement of surface-mount devices (SMDs), reflowing solder paste, and performing heat-based repairs (e.g., heat-shrink tubing).

TODO: Include pictures of different nozzles

<div class="grid cards" markdown>
-  ![Hot Air Rework Station](pictures/soldering/hot_air_rework_station.jpg){ width="40%" loading="lazy" }

    **Hot Air Rework Station**  
    The hot air rework station we have. You can control the temperature and airflow, and use different nozzles as well.
</div>

### Helping Hands

Helping hands are a tool that consists of a weighted base with adjustable arms and alligator clips. They are used to hold components, wires, or PCBs in place while soldering, allowing for better precision and stability. They are used when you wish you had a 3rd hand to hold something for you while soldering.


<div class="grid cards" markdown>
-  ![Helping Hands](pictures/soldering/helping_hands.jpg){ width="50%" loading="lazy" }

    **Helping Hands**  
    Plate with 4 adjustable arms with alligator clips, used to hold components in place while soldering.

-  ![Vise](pictures/soldering/vise.jpg){ width="40%" loading="lazy" }

    **Vise**  
    A more heavy-duty option for holding PCBs or components in place while soldering. The 2 knobs control the angle and the width of the grip.
</div>

### Microscope

A microscope can be an invaluable tool for soldering, especially when working with small components or fine-pitch soldering. It allows you to see the details of your work more clearly, ensuring better precision and quality in your [solder](#solder) joints.

<div class="grid cards" markdown>
-  ![Microscope](pictures/soldering/microscope.jpg){ width="25%" loading="lazy" }

    **Elikliv Microscope**  
    
    This microscope goes up to 1000x magnification. Focus is controlled by the knob on the bottom, and the arm height can be adjusted by the knob on the side.

</div>

### Soldering Mat

A soldering mat is a heat-resistant surface that provides a safe and organized workspace for soldering. It helps protect your work surface from heat damage, solder splashes, and provides a non-slip area to work on.

<div class="grid cards" markdown>
-  ![Soldering Mat](pictures/soldering/soldering_mat.jpg){ width="40%" loading="lazy" }

    **Soldering Mat**  
    
    The 2 soldering mats we have in the lab. The Digikey mat is preferred since it is made of silicone
</div>