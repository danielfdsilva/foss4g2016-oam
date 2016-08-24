## What problem are we trying to solve?
Need to have open and up to date imagery for disaster response.

Imagery from satellites, unmanned aerial vehicles (UAVs) and other aircraft is becoming increasingly available after a disaster. However it is often difficult to determine what is available, accessible and how to access it. OpenAerialMap (OAM) seeks to solve this by providing a simple open way to process and provide imagery for humanitarian response and disaster preparedness.

Anyone can contribute with imagery which is where OIN comes into play.
(maybe explain the difference between contributing with a node and through the uploader? would here be the right place?)

## What is OIN?
OIN is a network of openly licensed imagery.
Stripping it down is a standard of how imagery is shared through nodes.
It is meant to be a distributed system in the sense that any person/entity can host an imagery node.

All they have to do is follow the OIN standard, release the imagery under CC-BY-4.0, and add the node information to the register.

Essentially there are 2 main ways to contribute imagery:
- host you own node with imagery
- if you can't do that, you can use the OAM uploader form. (go over at the end)


**is this part of OAM? why a different name?**
>> Think of OIN as the foundation of imagery that OAM is built upon. OAM is just one way to leverage open imagery and provide an index of open imagery. But in theory there could be other ways that people use a commons of imagery. 

## What is OAM?
Set of tools for finding and sharing said imagery.

We have the catalog which indexes imagery from OIN and enables quick and simple ways to access it through multiple avenues

  - allows search by different params
  - filtering

and the browser which displays imagery. 

## OAM browser as a solution
We had the imagery and a way to search for it, now we needed a way to display it.
The oam browser provides a simple and easy way for users to find and download / use imagery.

[quick demo of how it works / capabilities]

## UI UX considerations while creating the grid

- Inspiration
  - blog post (https://developmentseed.org/blog/2015/06/05/designing-openaerialmap/)

- Why this grid system?
- How it came to be / origin? https://github.com/hotosm/OpenAerialMap/issues/26
  - problem with different ratios and areas.
  - problem navigating the map with so many different sizes.
  - different sensors, can't normalize.
  - infographic grid, heatmap like

3 different iterations:
- geographic grid. All cells had the same area and was a problem because their shape changed as the user panned across the planet.
- pixel grid. All the cells have the same visual size, regardless of the area they cover. Although not a accurate grid it's easier for the user.
- pixel grid with adjusting size.

## tech stack / why react
what should we say about the tech stack? Should we include references to travis as well? is that even interesting?
We used react because we wanted to try it out (https://github.com/developmentseed/oam-internal/issues/17). How do we make it sound like we picked the right tool for the job?

  - open, good community, growing and stable
  - experimentation
  - It gives us unidirectional data flow which is amazing for rendering templates and keeping stuff clean.
  - Renders are somewhat pure. the same input data originates the same output. We know that there are no third party actions messing with the resulting code.
  - Centralized state (kind of. We're using reflux, not redux).

## The OAM ecosystem (in brief)
- uploader:
The uploader is a way to upload imagery to the OAM node in the OIN. If you have imagery but can't or don't want to host a node you can submit imagery using this form.
To reduce spam imagery the uploader is only available to authorized people, although an access token is easy to request.

- docs
centralized place with evergrowing info about all the tools in the ecosystem, including the design system.
in brief, the design system is a set of styles / guidelines / shareable code that is used throughout the OAM universe to ensure visual and behavioral consistency.

## How to get involved
Besides sharing imagery / hosting a node / contributing with code, what else is there? Something more community driven?



### Sources:


- HOT presentation: https://docs.google.com/presentation/d/1FNwlcZ4NiUrix29rs7dSsevVMbhnZE6H3EKO4IHhYh4
- OAM Technical Diagram: https://github.com/hotosm/OpenAerialMap/wiki/OAM-Technical-Diagram-(current-as-of-August-12,-2016)
- OAM Catalog: http://hotosm.github.io/OpenAerialMap/oam-components/oam-c/
- React reaction: https://github.com/developmentseed/oam-internal/issues/17
- OAM flyer: https://github.com/developmentseed/oam-internal/issues/35
- Testing layer interactions: https://github.com/hotosm/OpenAerialMap/issues/26