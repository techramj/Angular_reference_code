# 1 add the  link and style
1. add the below line in index.html in head tag

        <link rel="preconnect" href="https://fonts.googleapis.com" />
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
        <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap"
            rel="stylesheet" />

2. styles.css

        {
            box-sizing: border-box;
        }

        html {
            height: 100%;
        }

        body {
            font-family: "Poppins", sans-serif;
            background: radial-gradient(circle at top left, #181023, #0b0519);
            color: #c3b3d8;
            margin: 0;
            padding: 0;
            height: 100%;
        }

3. app.component.css
```
main {
  width: 90%;
  max-width: 50rem;
  margin: 2.5rem auto;
  display: grid;
  grid-auto-flow: row;
  gap: 2rem;
}

#users {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  gap: 0.5rem;
  overflow: auto;
}

@media (min-width: 768px) {
  main {
    margin: 4rem auto;
    grid-template-columns: 1fr 3fr;
  }

  #users {
    flex-direction: column;
  }
}

```

# 2 create the header component
1. css
```
header {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    width: 90%;
    max-width: 50rem;
    margin: 0 auto 2rem auto;
    text-align: center;
    background: linear-gradient(
        to bottom,
        #2c0a4c,
        #450d80
    );
    padding: 1rem;
    border-bottom-right-radius: 12px;
    border-bottom-left-radius: 12px;
    box-shadow: 0 1px 8px rgba(0, 0, 0, 0.6);
    }

    img {
    width: 3.5rem;
    object-fit: contain;
    }

    h1 {
    font-size: 1.25rem;
    margin: 0;
    padding: 0;
    }

    p {
    margin: 0;
    font-size: 0.8rem;
    text-wrap: balance;
    }

    @media (min-width: 768px) {
    header {
        padding: 2rem;
    }

    img {
        width: 4.5rem;
    }

    h1 {
        font-size: 1.5rem;
        margin: 0;
        padding: 0;
    }
}
```
2. add the image in public folder

![alt text](img/task-management-logo.png)

3. create the header component ts, hmtl, css file.

***

# 2. User componenet
1. create the user componet using angular cli
``` 
ng g c user
```
2. user.component.style
```
div {
  border-radius: 6px;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

button {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.35rem 0.5rem;
  background-color: #433352;
  color: #c3b3d1;
  border: none;
  font: inherit;
  cursor: pointer;
  width: 100%;
  min-width: 10rem;
  text-align: left;
}

button:hover,
button:active,
.active {
  background-color: #9965dd;
  color: #150722;
}

img {
  width: 2rem;
  object-fit: contain;
  border-radius: 50%;
  box-shadow: 0 1px 8px rgba(0, 0, 0, 0.3);
}

span {
  margin: 0;
  padding: 0;
  font-size: 0.8rem;
  font-weight: normal;
}

```
# tasks. component.css
```
#tasks {
  padding: 1rem;
  border-radius: 8px;
  max-height: 60vh;
  overflow: auto;
  background-color: #3a2c54;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 2rem;
  gap: 1rem;
}

h2 {
  margin: 0;
  font-size: 0.9rem;
  width: 60%;
  text-wrap: balance;
}

menu {
  margin: 0;
  padding: 0;
}

menu button {
  font: inherit;
  cursor: pointer;
  background-color: #9965dd;
  border-radius: 4px;
  border: none;
  padding: 0.35rem 0.8rem;
  font-size: 0.9rem;
}

menu button:hover,
menu button:active {
  background-color: #a565dd
}

ul {
  list-style: none;
  margin: 1rem 0;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  max-height: 50vh;
  overflow: auto;
}

@media (min-width: 768px) {
  h2 {
    font-size: 1.25rem;
  }

  menu {
    width: auto;
  }
}
```

# Task.component.css
```
article {
  padding: 1rem;
  color: #25113d;
  background-color: #bf9ee5;
}

h2 {
  margin: 0;
}

time {
  color: #3c2c50;
}

.actions {
  text-align: right;
  margin: 0;
}

.actions button {
  font: inherit;
  font-size: 0.9rem;
  cursor: pointer;
  background-color: #380774;
  color: #decdf2;
  border-radius: 4px;
  padding: 0.5rem 1.5rem;
  border: none;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
}

.actions button:hover,
.actions button:active {
  background-color: #4a0774;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.3);
}
```

# new-task.css
```.backdrop {
  background-color: rgba(0, 0, 0, 0.9);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
}

dialog {
  width: 90%;
  max-width: 30rem;
  background-color: #433352;
  border-radius: 6px;
  border: none;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.4);
  overflow: hidden;
  padding: 1rem;
  top: 5rem;
}

h2 {
  margin: 0;
  color: #d0c2e1;
}

label {
  display: block;
  font-weight: bold;
  font-size: 0.85rem;
  color: #ab9ac0;
}

input,
textarea {
  width: 100%;
  font: inherit;
  padding: 0.15rem 0.25rem;
  border-radius: 4px;
  border: 1px solid #ab9ac0;
  background-color: #d0c2e1;
}

.actions {
  margin: 1rem 0 0;
  display: flex;
  justify-content: flex-end;
  gap: 0.25rem;
}

button {
  font: inherit;
  cursor: pointer;
  border: none;
  padding: 0.35rem 1.25rem;
  border-radius: 4px;
  background-color: transparent;
}

button[type="button"] {
  color: #bdadcf;
}

button[type="button"]:hover,
button[type="button"]:active {
  color: #d0c2e1;
}

button[type="submit"] {
  background-color: #9c73ca;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
  transition: all 0.3s ease;
}

button[type="submit"]:hover,
button[type="submit"]:active {
  background-color: #895cce;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.3);
}

@media (min-width: 768px) {
  dialog {
    padding: 2rem;
  }
}

```

# user-tasks.component.css
```
#tasks {
  padding: 1rem;
  border-radius: 8px;
  max-height: 60vh;
  overflow: auto;
  background-color: #3a2c54;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 2rem;
  gap: 1rem;
}

h2 {
  margin: 0;
  font-size: 0.9rem;
  width: 60%;
  text-wrap: balance;
}

menu {
  margin: 0;
  padding: 0;
}

menu a {
  font: inherit;
  cursor: pointer;
  color: #181223;
  background-color: #9965dd;
  border-radius: 4px;
  border: none;
  padding: 0.35rem 0.8rem;
  font-size: 0.9rem;
  text-decoration: none;
}

menu a:hover,
menu a:active {
  background-color: #a565dd
}

@media (min-width: 768px) {
  h2 {
    font-size: 1.25rem;
  }

  menu {
    width: auto;
  }
}
```





