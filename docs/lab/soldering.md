# Soldering

Soldering is the process of joining two or more electronic components together by melting a filler metal (solder) to create a strong electrical and mechanical bond.

This guide will cover the basics of soldering, including the tools and materials needed, the steps to soldering, some tips for achieving good results, and of course safety precautions.

## Tools and Materials

There are several tools and materials that you will need for soldering. Here are some of the most common ones:

### Solder

Solder is typically a metal alloy, often made of tin and optionally, lead. It comes in the form of a thin wire or a paste and is used to create a strong bond between electronic components.

Here are 3 types of solder we have in the lab:

<div class="grid cards" markdown>

-   ![Unleaded 0.3 mm](../pictures/soldering/unleaded_solder_0.3mm.jpg){ width="70%" loading="lazy" }

    **Unleaded 0.3 mm**  
    Fine pitch work, high melting point

-   ![Leaded 0.8 mm](../pictures/soldering/leaded_solder_0.8mm.jpg){ width="70%" loading="lazy" }

    **Leaded 0.8 mm**  
    Easier flow, stronger joints

-   ![Solder paste](../pictures/soldering/solder_paste.jpg){ width="70%" loading="lazy" }

    **Solder paste**  
    For sensitive SMD components, requires a reflow oven or hot air rework station

</div>

When should you use what solder? It depends on the application. 

For fine pitch work, such as soldering small SMD components, a thinner solder (like 0.3 mm) is often preferred for better control and precision.

For general-purpose soldering, a thicker solder (like 0.8 mm) can be easier to work with and provides stronger joints. 

Solder paste is typically used for surface mount devices (SMDs) and requires specialized equipment for reflow soldering, such as a [reflow oven]() or a [hot air rework station]().

The choice between leaded and unleaded solder depends on personal preference. It is much easier to work with leaded solder since it has a lower melting point and better flow characteristics. 

!!! warning "Lead Safety"
    Leaded solder contains lead, which is toxic. Always **wash** your hands after handling leaded solder, since there are fine particulates that can settle on your fingers. Always use a [fume extractor]() when soldering to avoid inhaling flux fumes.

### Soldering Iron

A soldering iron is a handheld tool that heats up to melt solder. It typically has a pointed tip that allows for precise application of heat to the components being soldered.

We have 2 good soldering irons in the lab:

<div class="grid cards" markdown>

-  ![TC 22 Soldering Station](../pictures/soldering/TC22_soldering_station.jpg){ width="70%" loading="lazy" }

    **TC 22 Soldering Station**  
    Digital display, extremely fast heat up time, needs a power outlet

- ![Pinecil soldering station](../pictures/soldering/pinecil_soldering_iron.jpg){ width="70%" loading="lazy" }

    **Pinecil Soldering Station**  
    Compact, portable, and USB-C powered (needs a good 35W+ PD cable).

</div>

### Flux

Flux is a chemical agent that helps to clean, remove oxides, promotes wetting, and improves the flow of solder and the quality of the joint. It can come in various forms, such as liquid, paste, or as a core in solder wire.

We have 2 types of flux in the lab:

<div class="grid cards" markdown>
-  ![Flux pen](../pictures/soldering/flux_pen.jpg){ width="70%" loading="lazy" }

    **Flux Pen**  
    Depress the tip to release flux, needs cleaning after soldering
  
- ![No-Clean Flux](../pictures/soldering/no_clean_flux.jpg){ width="70%" loading="lazy" }

    **No-Clean Flux**  
    Suitable for general use, does not require cleaning after soldering.
</div>


### Solder Wick

Solder wick, also known as desoldering braid, is a braided copper wire that is used to remove excess solder from a joint. It works by absorbing the molten solder when heated with a soldering iron.

<div class="grid cards" markdown>
-  ![Solder Wick](../pictures/soldering/solder_wick.jpg){ width="70%" loading="lazy" }

    **Solder Wick**  
    The copper braid absorbs molten solder
</div>


### Solder Sucker

A solder sucker, also known as a desoldering pump, is a handheld tool that creates suction to remove molten solder from a joint. It typically consists of a plunger and a nozzle that can be placed over the molten solder to be removed.

<div class="grid cards" markdown>
-  ![Solder Sucker](../pictures/soldering/solder_sucker.jpg){ width="70%" loading="lazy" }

    **Solder Sucker**  
    Press the plunger to create suction, place the nozzle over molten solder, and release the plunger to suck up the solder.
-  ![Old Solder Sucker](../pictures/soldering/old_solder_sucker.jpg){ width="70%" loading="lazy" }

    **Old Solder Sucker**  
    A more traditional design, but can be less effective since the suction isn't as strong.
</div>

### Fume Extractor
