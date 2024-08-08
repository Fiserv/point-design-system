# Design System

A design system is a complete set of design standards (style guide) and documentation accompanying a UI tool kit, including UI patterns, UX design principles, and components. When we look at a design system in this context, it incorporates everything designers and developers need to build and scale digital products. Some of things you will find within a design system includes:

- Accessibility guidelines
- UI Design guidelines
- Governance & Best Practices
- Design system roadmap and releases
- Code snippets
- CSS variables & design tokens
- UI kit (an image-based version of design system components)
- Downloadable assets

| Building Blocks      | UI Patterns | Rules                |
| :------------------- | :---------- | :------------------- |
| Editorial Guidelines | Templates   | Design Principles    |
| Color Schemes        | Modules     | Implementation       |
| Grid Definition      | Components  | Dos and Don'ts       |
| Icons/Image Assets   | Elements    | Editorial Guidelines |

## Pattern library versus component library

Another big cause for confusion is “the difference between a pattern library vs. a component library.” Most designers use these terms interchangeably. That is correct, but it is also not completely accurate. The difference between components and patterns is best explained using Brad Frost’s Atomic Design methodology.

- **Atoms**
In Atomic Design, as in chemistry, atoms are the basic elements that help inform everything. In the world of web applications, atoms are the foundational elements, such as HTML tags, fonts, animations, and color palettes. Web design “atoms” can also be less concrete. Examples include buttons or forms.

- **Molecules**
Are the next-largest building block. Created by the joining of different atomic elements, molecules are complex by nature. Because they are the product of various atoms, though, it is possible to break them down, conceptually, into UI elements that are easier to digest. Examples of web design molecules include the things that become the backbone of the larger design system, such as form labels or input field.

- **Organisms**
Atoms combine to form molecules, and groups of molecules form organisms. In Atomic Design, organisms are the UI elements that shape a website's appearance and functionality. They are also the elements that start to impact user interface. The way a developer arranges molecules informs the site experience and the complexity of the finished product. Examples of organisms include logos, search fields, and main navigation which together may form a header organism.

- **Templates**
At this phase of the Atomic Design process, we start to break with the chemistry analogy and shift back into the lexicon of front-end development. Templates, then, are “organisms” strung together at the page-level or beyond. Templates, online atoms, organisms, and molecules are highly concrete. They provide a fixed context for the more abstract pieces to fit and are responsible for pulling the site together into something resembling its final form. An HTML wireframe is an excellent example of a template.

- *Pages*
Finally, are the final element of Atomic Design. According to Brad Frost himself, pages are the specific instances of templates. Pages are the most tangible element of all and are the places users spend most of their time. They are also one of the most essential phases of the Atomic Design process since the final iteration of pages is where developers get to see whether the entire design system is effective or not. In short, the final appearance of the pages dictates whether the product design is ready to launch, or whether the developer needs to loop back and make changes to earlier UI design elements.

Using Atomic Design, we can define patterns and components as follows:

- **Component library (Atoms)** - A component is a reusable block of code that can stand alone or form part of multiple UI patterns–for example, a button. A component library is a collection of UI components within a design system.

- **Pattern library (Molecules and Organisms)** - A component is a reusable block of code that can stand alone or form part of multiple UI patterns–for example, a button. A component library is a collection of UI components within a design system.

## Style guide

And lastly, we have a style guide. A style guide is a piece of documentation that provides context and instructions for a design system’s patterns and components–for example, color HEX codes, typography scales, usage, etc.

## Design systsem versus component library

When people talk about component libraries like MUI, React-Bootstrap, and others, things get even more confusing. Aren’t these design systems?

Although these component libraries have extensive documentation and guidelines, they are not design systems. Designers and engineers can use these open-source component libraries however they choose.

They can edit the library’s components without limitations (so that they are indistinguishable from the original), build new patterns, combine with other libraries, or create custom components.

The design system is different. Designers and engineers must use the components as building blocks. They must follow the system’s guidelines, style guide, principles, and other documentation to design consistent-looking user interfaces–like following the instructions to build a Lego set.

If team members want to change a component or introduce a new pattern, they must follow the design system’s governance procedures. In some cases, the design system team will have the final say about how to build that new component.

## Design systems in practical sense

Design systems might seem restrictive, but there is a good reason for these processes and protocols. Let us take Atlassian as an example. Atlassian has a suite of business tools with a global userbase.

The company’s biggest selling point is that organizations can use and sync Atlassian’s product suite for a cohesive, consistent experience across the company, from customer support to sales, design, and development.

It is challenging to achieve that level of consistency when you have a global team of designers, product teams, and engineers. So, Atlassian’s design system stipulates how teams must design its products for a seamless user experience.

In another example, Shopify allows third-party applications, themes, and other integrations. These add-ons come from freelancers and agencies worldwide–which is even more challenging to maintain cohesion and consistency than Atlassian!

Shopify developed its design system Polaris to ensure a consistent user experience, which both internal and third-party developers use to build Shopify products. The design system includes a UI kit for designers and React component library for engineers.

In this case, Polaris is the complete design system of principles, written content, visual properties, and UI components. The style guide is the static documentation on the Polaris website describing how to use the design system. The pattern library is part of the “Components” in the Polaris design system.

The differences are subtle but unmistakably important when it comes to improving product development. A style guide on its own becomes quickly outdated since documentation requires maintenance. A pattern library lacks the instructions and principles for coherent implementation.

## Creating a design system

1. **Create the UI inventory** - First list and describe all the design patterns currently used in your interface and note the inconsistencies therein.

2. **Get support of the organization** - Present your findings and explain the utility of a common design language to everyone. Estimate the number of design and engineering hours wasted on redundant work and how product coherence can improve NPS scores.

3. **Establish design principles** - Codify your practices. You are now starting to work on the style guide for the design system.

4. **Build the color palette** - When building the UI inventory, we found 116 different shades of grey that needed consolidation. Create the palette and its naming convention.

5. **Build the typographic scale** - You can optimize the scale to serve existing styles, or you might try to build a harmonious scale using the golden ratio or major second. When building the scale, do not forget that you are not only setting the size of the font, but also weight, line-height, and other properties.

6. **Implement icons library and other styles** - Decide which icons from the UI inventory will become part of the design system, then standardize the implementation.

7. **Start building your first patterns** - This is the task that will never end. Patterns should always either reflect the truth about the product or reflect the aspirational state of the product soon.

## Using the design system

Designers and engineers follow the same design principles, but the guidelines and documentation differ. 

For example, with Polaris, designers and engineers must follow Foundations and Experiences to understand the principles, brand requirements, and approach to designing Shopify products. This knowledge is essential to know before you can start designing and coding. 

Polaris also includes a Resources section with a UI kit, Polaris tools (icons set), Polaris GitHub page, links to Shopify’s blogs, additional developer documentation, and forums/communities.

## Using a component library

Component libraries provide design and engineering teams with a comprehensive collection of UI elements and components for digital product design.
 
The most significant benefit is that teams do not have to start from nothing–they can begin prototyping and testing immediately using a thoroughly tested component library.

MUI (based on Google’s Material Design UI), one of the world’s most comprehensive and widely used component libraries, even provides customization through theming, so you can separate your UIs (User Interface) (User Interface) from competitors–even if they are using the same component library.

While component libraries are customizable, they also provide a sole source of truth between design and development–something particularly challenging, especially in the initial stages of a product’s lifecycle.
 
Using the same components as engineers gives designers some constraints to minimize drift. At design handoff, engineers simply copy the component library’s components and make changes according to the designer’s mockups and prototypes.

Another significant benefit of a component library is that it gives solo engineers and startups professionally styled UI elements to build products and prototypes, making it easier to enter the market and compete.



