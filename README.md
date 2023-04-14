# SMACSS Structure

```
css/
|-- base/
|   |-- reset.css
|   |-- typography.css
|-- layout/
|   |-- header.css
|   |-- footer.css
|-- modules/
|   |-- button.css
|   |-- carousel.css
|   |-- form.css
|-- state/
|   |-- hover.css
|   |-- active.css
|-- theme/
|   |-- light.css
|   |-- dark.css
|-- pages/
|   |-- home.css
|   |-- about.css
|   |-- contact.css
|-- components/
|   |-- card/
|   |   |-- card.css
|   |   |-- card-theme.css
|   |-- hero/
|   |   |-- hero.css
|   |   |-- hero-theme.css
|-- main.css
```

# Component-Based Structure
```
css/
|-- components/
|   |-- button/
|   |   |-- button.css
|   |   |-- button-variant.css
|   |   |-- button-theme.css
|   |-- card/
|   |   |-- card.css
|   |   |-- card-theme.css
|-- main.css
```

# BEM - Naming Convention for CSS classes

> Example of a page   

```
<div class="header">
  <h1 class="header__logo">My Website</h1>
  <nav class="header__nav">
    <ul class="header__nav-list">
      <li class="header__nav-item"><a href="#" class="header__nav-link">Home</a></li>
      <li class="header__nav-item"><a href="#" class="header__nav-link">About</a></li>
      <li class="header__nav-item"><a href="#" class="header__nav-link">Services</a></li>
      <li class="header__nav-item"><a href="#" class="header__nav-link">Contact</a></li>
    </ul>
  </nav>
</div>

<section class="hero">
  <h2 class="hero__title">Welcome to My Website</h2>
  <p class="hero__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam commodo fermentum felis, nec vulputate lorem consequat sit amet.</p>
  <a href="#" class="hero__cta">Learn More</a>
</section>

<section class="services">
  <h2 class="services__title">Our Services</h2>
  <ul class="services__list">
    <li class="services__item">
      <h3 class="services__item-title">Web Design</h3>
      <p class="services__item-description">We create modern and responsive websites tailored to your business needs.</p>
    </li>
    <li class="services__item">
      <h3 class="services__item-title">Graphic Design</h3>
      <p class="services__item-description">We provide creative and visually appealing graphic design services.</p>
    </li>
    <li class="services__item">
      <h3 class="services__item-title">Digital Marketing</h3>
      <p class="services__item-description">We offer effective digital marketing strategies to grow your online presence.</p>
    </li>
  </ul>
</section>

<footer class="footer">
  <div class="footer__logo">My Website</div>
  <p class="footer__text">Contact us: info@mywebsite.com</p>
</footer>
```

> Example of a component to be used in various pages    

In this example, we're using the "card" as the main block name for the component, and "image", "title", "description", and "cta" as the element names for the different parts of the card component. The double underscore "__" is used to separate the block name and element name in BEM convention.    

```
<!-- Card Component -->
<div class="card">
  <img src="card-image.jpg" alt="Card Image" class="card__image">
  <h3 class="card__title">Card Title</h3>
  <p class="card__description">Card Description</p>
  <a href="#" class="card__cta">Learn More</a>
</div>
```

Then, when you use this card component in different sections of your website, you can prefix the block name with the name of the section to create a unique class name for each usage. For example:   


```
<!-- Hero Section -->
<section class="hero">
  <!-- Card Component used in the hero section -->
  <div class="hero__card card">
    <!-- card content -->
  </div>
</section>

<!-- Services Section -->
<section class="services">
  <!-- Card Component used in the services section -->
  <div class="services__card card">
    <!-- card content -->
  </div>
</section>

<!-- Testimonials Section -->
<section class="testimonials">
  <!-- Card Component used in the testimonials section -->
  <div class="testimonials__card card">
    <!-- card content -->
  </div>
</section>
```

```
<h1>Hello, World!</h1>
<p>This is an example HTML code.</p>
```
