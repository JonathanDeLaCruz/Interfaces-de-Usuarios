# Primeros pasos con Tailwind

## Requisitos

* [nodeJS](https://nodejs.org/en/download/prebuilt-installer/current)
* [Visual Studio Code](https://code.visualstudio.com/)

## Primer proyecto con Tailwind

* Creamos la carpeta donde trabajaremos el proyecto y abrimos la terminal

```javascript
  npm install tailwindcss --save
```

* Añadiendo Tailwind, creamos un archivo main.css y agregamos lo siguiente:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

* Creamos el archivo de configuración y procesamiento del CSS de Tailwind

```javascript
npx tailwindcss init
```

* Modificamos el archivo que se acaba de crear y añadimos los archivos que tendran acceso a los estilos de Tailwind

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ['*.html', '*.js'],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

* Incluimos el CSS de Tailwind en el index.html

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="dist/tailwind.css">
  
</head>
<body>
    <header>
        <nav class="flex items-center justify-between p-6 container mx-auto">
            <!-- Logo -->
            <svg class="h-10 w-10" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 54 64">
                <defs>
                    <style>
                        .cls-1 {
                            fill: #319795;
                        }
    
                        .cls-2,
                        .cls-4 {
                            fill: #2a344f;
                        }
    
                        .cls-2 {
                            opacity: 0.32;
                            isolation: isolate;
                        }
    
                        .cls-3 {
                            opacity: 0.16;
                        }
                    </style>
                </defs>
                <title>logo</title>
                <g id="Layer_2" data-name="Layer 2">
                    <g id="Layer_1-2" data-name="Layer 1">
                        <g id="Group_16" data-name="Group 16">
                            <g id="Group_15" data-name="Group 15">
                                <g id="Group_12" data-name="Group 12">
                                    <path id="Path_35" data-name="Path 35" class="cls-1"
                                        d="M53.52,1.87l-22,5.39a1.61,1.61,0,0,1-1.23-.21L19.89.25a1.57,1.57,0,0,0-1.3-.19l-18,5.3A.77.77,0,0,0,0,6.09V16.87L18.59,11.4a1.57,1.57,0,0,1,1.3.19l10.4,6.79a1.53,1.53,0,0,0,1.23.21L54,13.09V2.23a.39.39,0,0,0-.39-.38Z">
                                    </path>
                                    <path id="Path_36" data-name="Path 36" class="cls-1"
                                        d="M40.25,27.84l-8.73,2.1a1.57,1.57,0,0,1-1.23-.21l-10.4-6.8a.37.37,0,0,0-.53.11.31.31,0,0,0-.07.2V33.47a.75.75,0,0,0,.34.63l10.66,7a1.57,1.57,0,0,0,1.23.2l9.23-2.21A6.86,6.86,0,0,0,46,32.45v-.21a4.62,4.62,0,0,0-4.68-4.55A4.93,4.93,0,0,0,40.25,27.84Z">
                                    </path>
                                    <path id="Path_37" data-name="Path 37" class="cls-1"
                                        d="M40.25,50.52l-8.73,2.1a1.61,1.61,0,0,1-1.23-.21l-10.4-6.8a.38.38,0,0,0-.53.1.35.35,0,0,0-.07.21V56.15a.75.75,0,0,0,.34.63l10.66,7a1.53,1.53,0,0,0,1.23.21l9.23-2.22A6.84,6.84,0,0,0,46,55.13v-.21a4.62,4.62,0,0,0-4.68-4.55A4.39,4.39,0,0,0,40.25,50.52Z">
                                    </path>
                                </g>
                                <path id="Path_38" data-name="Path 38" class="cls-2"
                                    d="M30.86,41.29V30a1.63,1.63,0,0,0,.66,0L35.28,29l2.2,10.8-6,1.46A1.47,1.47,0,0,1,30.86,41.29Zm8.82,9.33-8.16,2a1.63,1.63,0,0,1-.66,0V64a1.63,1.63,0,0,0,.66,0l10.36-2.54Zm-8.82-32a1.63,1.63,0,0,0,.66,0l1.57-.38L30.86,7.28Z">
                                </path>
                                <g id="Group_13" data-name="Group 13" class="cls-3">
                                    <path id="Path_39" data-name="Path 39" class="cls-4"
                                        d="M19.29,11.36a1.82,1.82,0,0,1,.6.23l10.4,6.8a1.41,1.41,0,0,0,.57.22V7.27a1.41,1.41,0,0,1-.57-.22L19.89.25a1.82,1.82,0,0,0-.6-.23Z">
                                    </path>
                                    <path id="Path_40" data-name="Path 40" class="cls-4"
                                        d="M30.86,52.64a1.67,1.67,0,0,1-.57-.23l-10.4-6.8a.39.39,0,0,0-.54.11.36.36,0,0,0-.06.2V56.15a.75.75,0,0,0,.34.63l10.66,7a1.73,1.73,0,0,0,.57.22Z">
                                    </path>
                                    <path id="Path_41" data-name="Path 41" class="cls-4"
                                        d="M19.89,22.93a.39.39,0,0,0-.54.11.36.36,0,0,0-.06.2V33.47a.75.75,0,0,0,.34.63l10.66,7a1.58,1.58,0,0,0,.57.22V30a1.43,1.43,0,0,1-.57-.23Z">
                                    </path>
                                </g>
                            </g>
                        </g>
                    </g>
                </g>
            </svg>
    
            <!-- Menu items -->
            <div class="text-lg text-gray-600 hidden lg:flex">
                <a href="#" class="block mt-4 lg:inline-block text-teal-600 lg:mt-0 mr-10">
                    Home
                </a>
                <a href="#" class="block mt-4 lg:inline-block hover:text-gray-700 lg:mt-0 mr-10">
                    Services
                </a>
                <a href="#" class="block mt-4 lg:inline-block hover:text-gray-700 lg:mt-0 mr-10">
                    Portfolio
                </a>
                <a href="#" class="block hover:text-gray-700 mt-4 lg:inline-block lg:mt-0 mr-10">
                    Company
                </a>
                <a href="#" class="block hover:text-gray-700 mt-4 lg:inline-block lg:mt-0">
                    Contact
                </a>
            </div>
    
            <!-- CTA and Hamburger icon -->
            <div class="flex items-center">
                <div class="mr-5 lg:mr-0">
                    <button class="py-2 px-6 rounded-md text-gray-600 hover:text-gray-700 text-lg">Sign in</button>
                    <button class="py-2 px-6 bg-teal-500 hover:bg-teal-600 rounded-md text-white text-lg">Sign up</button>
                </div>
                <div class="block lg:hidden">
                    <button
                        class="flex items-center px-4 py-3 border rounded text-teal-500 border-teal-500 focus:outline-none">
                        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                            <title>Menu</title>
                            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                        </svg>
                    </button>
                </div>
            </div>
        </nav>
    </header>
    <div class="overflow-hidden bg-white py-24 sm:py-32">
        <div class="mx-auto max-w-7xl px-6 lg:px-8">
          <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2">
            <div class="lg:pr-8 lg:pt-4">
              <div class="lg:max-w-lg">
                <h2 class="text-base font-semibold leading-7 text-indigo-600">Deploy faster</h2>
                <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">A better workflow</p>
                <p class="mt-6 text-lg leading-8 text-gray-600">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.</p>
                <dl class="mt-10 max-w-xl space-y-8 text-base leading-7 text-gray-600 lg:max-w-none">
                  <div class="relative pl-9">
                    <dt class="inline font-semibold text-gray-900">
                      <svg class="absolute left-1 top-1 h-5 w-5 text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                        <path fill-rule="evenodd" d="M5.5 17a4.5 4.5 0 0 1-1.44-8.765 4.5 4.5 0 0 1 8.302-3.046 3.5 3.5 0 0 1 4.504 4.272A4 4 0 0 1 15 17H5.5Zm3.75-2.75a.75.75 0 0 0 1.5 0V9.66l1.95 2.1a.75.75 0 1 0 1.1-1.02l-3.25-3.5a.75.75 0 0 0-1.1 0l-3.25 3.5a.75.75 0 1 0 1.1 1.02l1.95-2.1v4.59Z" clip-rule="evenodd" />
                      </svg>
                      Push to deploy.
                    </dt>
                    <dd class="inline">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.</dd>
                  </div>
                  <div class="relative pl-9">
                    <dt class="inline font-semibold text-gray-900">
                      <svg class="absolute left-1 top-1 h-5 w-5 text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                        <path fill-rule="evenodd" d="M10 1a4.5 4.5 0 0 0-4.5 4.5V9H5a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h10a2 2 0 0 0 2-2v-6a2 2 0 0 0-2-2h-.5V5.5A4.5 4.5 0 0 0 10 1Zm3 8V5.5a3 3 0 1 0-6 0V9h6Z" clip-rule="evenodd" />
                      </svg>
                      SSL certificates.
                    </dt>
                    <dd class="inline">Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.</dd>
                  </div>
                  <div class="relative pl-9">
                    <dt class="inline font-semibold text-gray-900">
                      <svg class="absolute left-1 top-1 h-5 w-5 text-indigo-600" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                        <path d="M4.632 3.533A2 2 0 0 1 6.577 2h6.846a2 2 0 0 1 1.945 1.533l1.976 8.234A3.489 3.489 0 0 0 16 11.5H4c-.476 0-.93.095-1.344.267l1.976-8.234Z" />
                        <path fill-rule="evenodd" d="M4 13a2 2 0 1 0 0 4h12a2 2 0 1 0 0-4H4Zm11.24 2a.75.75 0 0 1 .75-.75H16a.75.75 0 0 1 .75.75v.01a.75.75 0 0 1-.75.75h-.01a.75.75 0 0 1-.75-.75V15Zm-2.25-.75a.75.75 0 0 0-.75.75v.01c0 .414.336.75.75.75H13a.75.75 0 0 0 .75-.75V15a.75.75 0 0 0-.75-.75h-.01Z" clip-rule="evenodd" />
                      </svg>
                      Database backups.
                    </dt>
                    <dd class="inline">Ac tincidunt sapien vehicula erat auctor pellentesque rhoncus. Et magna sit morbi lobortis.</dd>
                  </div>
                </dl>
              </div>
            </div>
            <img src="https://tailwindui.com/plus/img/component-images/dark-project-app-screenshot.png" alt="Product screenshot" class="w-[48rem] max-w-none rounded-xl shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem] md:-ml-4 lg:-ml-0" width="2432" height="1442">
          </div>
        </div>
      </div>
      
</body>
</html>
```

* Procesamos el css con Tailwind

```javascript
npx tailwindcss -i .\main.css -o ./dist/tailwind.css --minify
```
