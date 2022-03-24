## Adding Bootstrap NavBar in Angular Application

### Bootstrap components
Built into Bootstrap are a number of reusable elements, conveniently styled out with accompanying JS to easily add components such as navigations, alerts, dropdowns, buttons, responsive tables, lists, responsive media objects, and more! There are over 20 different Bootstrap components that can be found [here](https://getbootstrap.com/docs/5.0/components/navbar/):

### About this exercise
Previously we have installed the bootstrap and fontawesome in our angular application. 
> If you want to install bootstrap and fontawesome in an angular application you can [Click Here](https://github.com/PatternsTechGit/PT_Fontawesoome_Bootstrap "Click Here").

In this lab we will
- Use Bootstrap navbar component in Angular application.
- Make NavBar responsive and mobile friendly.

------------
#### Step 1: Generating a new Component
we will generate a new component in app folder using `ng g c` command named toolbar

```typescript
ng g c toolbar
```

![toolbarComponent](https://github.com/PatternsTechGit/PT_AngularCLI/blob/main/images/module_vs_component.png)

#### Step 2: Declaration of Component in App Module
After creating the component we have to import our component in the declaration array

![appmodule](https://github.com/PatternsTechGit/PT_AngularCLI/blob/main/images/module_vs_component.png)


#### Step 3: Placing navbar in App Component

#### Step 4: Desiging Navbar with Bootstrap
In the `toolbar.component.html` write the following bootstrap code for navBar Component

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">BBBank</a>
      
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto- mb-2 mb-lg-0 ms-5">

          <li class="nav-item dropdown d-flex flex-end">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="true">
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


#### Step 5: Styling our NavBar
In the `styles.css` in src folder, write the following css code for styling the navbar
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
a.sidenav-button {
    display: inline;
    color: rgba(255, 255, 255, .5);
    margin-right: 10px;
    transition: all .3s ease 0s;
}
a.sidenav-button:hover {
    color: rgba(255, 255, 255, .8);
    transition: all .3s ease 0s;
}
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

.ms-5 {
    margin-left: auto !important;
}
```
