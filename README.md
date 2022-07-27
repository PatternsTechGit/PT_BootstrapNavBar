# Adding Bootstrap NavBar in Angular Application

## Bootstrap components
Bootstrap is an HTML, CSS and JavaScript framework. Using it, you can easily build mobile-first responsive websites. It offers you plenty of pre-set CSS styling for web elements, including navigation bars. In this tutorial, you will learn how to easily create a basic **Bootstrap responsive navbar**.

There are over 20 different Bootstrap components that can be found [here](https://getbootstrap.com/docs/5.0/components/navbar/)


### About this exercise
**Previously** we have scaffolded a newly angular application and installed the bootstrap and fontawesome in it.

In this lab we will
- Use *Bootstrap navbar component* in Angular application.
- Make NavBar *responsive* and *mobile friendly*.

### How NavBar Works?
Navbar require a wrapping `.navbar` with `.navbar-expand{-sm|-md|-lg|-xl|-xxl}` for responsive collapsing and color scheme classes.

1. `.navbar` class define the navbar's component
2. `.navbar-expand` class can create navigation bar vertical depending on the screen size
------------


### Step 1: Generating a new Component
We will generate a new component for our NavBar in app folder using `ng g c` command named `toolbar`. For this open terminal and run this command

```typescript
ng g c toolbar
```

This will also *import toolbar component* in the declaration array in` app.module.ts` file.  
After that, we have to place the selector `<app-toolbar></app-toolbar>` of toolbar component in `app.component.html`

### Step 2: Designing Navbar Template
In the `toolbar.component.html` write the following HTML code for navBar Component

```html
<!-- .navbar -->

<!-- .navbar-expand class can create navigation bar vertical depending on the screen size -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">

      <!-- .navbar-brand class ids for company, product, or project name -->
      <a class="navbar-brand" href="#">BBBank</a>
      
      <!-- Toggler/collapsibe Button -->

      <!-- .navbar-toggler class is used to determine when the content toggles behind a button -->
      <!-- data-bs-target="" used to target the navbar content to collapse/Toggle when matches the content's id="" -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" 
                                                   data-bs-target="#navbarSupportedContent" 
                                                   aria-controls="navbarSupportedContent" 
                                                   aria-expanded="false" 
                                                   aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Navbar Content -->

      <!-- The .collapse .navbar-collapse classes are for grouping and hiding navbar contents by a parent breakpoint -->
      <!-- The id="" of navbar content should matches with the button data-bs-target="#" to work toggle properly -->
      <div class="collapse navbar-collapse" id="navbarSupportedContent">

        <!-- .navbar-nav class is for full-height and lightweight navigation (including support for dropdowns) -->
        <ul class="navbar-nav mb-2 mb-lg-0 ml-nav-custom">

          <li class="nav-item dropdown d-flex flex-end">
            
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" 
                                                data-bs-toggle="dropdown" aria-expanded="true">
                <div class="photo">
                    <img alt="Profile Photo" src="assets/images/profile.jpg" />
                </div>
                Raas Masood
            </a>

            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li><a class="dropdown-item" href="#">Profile</a></li>
              <li><a class="dropdown-item" href="#">Logout</a></li>
            </ul>

          </li>

        </ul>
      </div>

    </div>
  </nav>
```


### Step 3: Styling our Application

In the `styles.css` in **src folder** paste the following code for styling our application layout. This is global styling. 

```css
html, body { height: 100%; }
body {
  margin: 0;
  font-family: "Poppins", sans-serif;
  font-size: 0.875rem;
  font-weight: 400;
  line-height: 1.5;
  color: #525f7f;
  text-align: left;
  background-color: #1e1e2f;
}

.bg-dark {
    background-color: #1e1e2f !important;
}
```


### Step 4: Styling our NavBar Component
Now we will style our toolbar component. In the `toolbar.component.css` in file paste the following css code for styling the navbar

```css

/* Used to style profile photo in navbar */
.navbar .photo {
    display: inline-block;
    height: 30px;
    width: 30px;
    border-radius: 50%;
    vertical-align: middle;
    overflow: hidden;
}

.navbar .photo img {
    width: 100%;
}

/* Class to align photo icon left in navbar */
.ml-nav-custom {
    margin-left: auto !important;
}

```
## Final Output
After running the application our responsive navbar component made using bootstrap looks like

![NavBar](https://github.com/PatternsTechGit/PT_BootstrapNavBar/blob/main/Readme-images/navBar-desktop.png)


#### toolbar Component Output on mobile view
Now if your stretch down your browser or open this application on mobile phone your toolbar component's Output will looks like this. 

![NavBar](https://github.com/PatternsTechGit/PT_BootstrapNavBar/blob/main/Readme-images/navBar-mobile.png)
