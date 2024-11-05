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




