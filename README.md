# React Mortgage calculator Tutorial for beginners

## Table of Contents

* [Setup](#Setup)
* [Material UI Theme](#MUI-Theme)
* [Navbar](#Navbar)
* Slider Component

## Setup 

Inorder to setup the project we need to install react & material-ui. First create a folder named `mortgage-calculator` and then run the following command in the terminal

```bash
npx create-react-app .
npm install @mui/material @emotion/react @emotion/styled
npm install --save chart.js react-chartjs-2
```

## MUI Theme

We will be using the dark theme of material UI. For that we need to create a file named `theme.js` in the `src` folder and add the following code

#### theme.js

```js
import { createTheme } from '@mui/material/styles';

export const theme = createTheme({
  palette: {
    mode: 'dark',
  },
})
```

#### index.js

Next up, we need to import the theme in the `index.js` file and wrap the app with the theme provider. follow along 👇

```js
import { ThemeProvider } from "@mui/material/styles";
import CssBaseline from "@mui/material/CssBaseline";
import { theme } from "./theme";

<React.StrictMode>
  <ThemeProvider theme={theme}>
    <App />
    <CssBaseline />
  </ThemeProvider>
</React.StrictMode>
```

## Navbar

Next up, we will be creating a very simple Navbar to show the Logo. For that we need to create a file named `Navbar.js` in the `src/Components` folder and add the following code

```js
import AppBar from "@mui/material/AppBar";
import Toolbar from "@mui/material/Toolbar";
import Typography from "@mui/material/Typography";
import { Container } from "@mui/system";

const Navbar = () => {
  return (
    <AppBar position="static">
      <Container maxWidth='xl'>
        <Toolbar>
          <Typography variant="h5">
            Bank of React
          </Typography>
        </Toolbar>
      </Container>
    </AppBar>
  );
};

export default Navbar;
```

## Slider Component