# Movies App (Netflix/Amazon Prime Clone)

## _React-JS Mini Project_

A web application built using React JS that will fetch data from an internal server using a `class component`, displaying that data, using `component lifecycle methods`, `routing concepts`, `authentication and authorization`, and adding `responsiveness` to the website.

#### Design Files
- You can check the **Design Files** for different devices [here](https://www.figma.com/file/tPdVlj0p5PESmymNkHYVgk/Movies_App?node-id=0%3A1)

### Features

**Login Route**
<details>
<summary>Click to view</summary>

  - When an invalid username and password are provided and the **Login** button is clicked, then the respective error message received from the response will be displayed
  - When a valid username and password are provided and the **Login** button is clicked, then the page will be navigated to the Home Route
  - When an _unauthenticated_ user tries to access the Home Route, Popular Route, Search Route, Account Route and Movie Item Details Route, then the page will be navigated to Login Route
  - When an _authenticated_ user tries to access the Home Route, Popular Route, Search Route, Account Route and Movie Item Details Route, then the page will be navigated to the respective route
  - When an _authenticated_ user tries to access the Login Route, then the page will be navigated to the Home Route

</details>

**Home Route**
<details>
<summary>Click to view</summary>
  
  - When an authenticated user opens the Home Route,

    - An HTTP Get request will be made to **Trending Now Movies API URL**, **Originals API URL** with `jwt_token` in the Cookies

      - **_Loader_** will be displayed while fetching the each data
      - After the data is successfully fetched from both the API's
        - A **random** movie title and movie poster with its details will be displayed from the **Originals Response**
        - Displayed the list of movies received from the Trending Now Movies Response
        - Displayed the list of movies received from the Originals Response
      - If any of the HTTP GET request made is unsuccessful, then the failure view given in the **Figma** screens will be displayed respectively
        - When the **Try Again** button is clicked, then the respective HTTP GET request will be made
    - When a **Movie** item is clicked, then the page will be navigated to the Movie Item Details Route
    
</details>


**Header**
<details>
<summary>Click to view</summary>
  
- When the **Movies** logo in the header is clicked, then the page will be navigated to the Home Route
- When the **Home** link in the Header is clicked, then the page will be navigated to the Home Route
- When the **Popular** link in the header is clicked, then the page will be navigated to the Popular Route
- When the **Search** icon in the header is clicked, then the page will be navigated to the Search Route
- When the **Profile** logo in the header is clicked, then the page will be navigated to the Account Route

</details>


**Popular Route**
<details>
<summary>Click to view</summary>
  
  - When an authenticated user opens the Popular Route

    - An HTTP GET request will be made to **Popular Movies API URL** with `jwt_token` in the Cookies

      - **_Loader_** will be displayed while fetching the data
      - After the data is fetched successfully, the response received will be displayed
      - If the HTTP GET request made is unsuccessful, then the failure view given in the **Figma** screens will be displayed
        - When the **Try Again** button is clicked, an HTTP GET request will be made to **Popular Movies API URL**

    - When a **Movie** item is clicked, then the page will be navigated to the Movie Item Details Route
    - All the header functionalities mentioned in the Home Route will work in this route accordingly
    
</details>


**Movie Item details Route**
<details>
<summary>Click to view</summary>
  
  - When an authenticated user opens the Movie Item Details Route

    - An HTTP GET request will be made to **Movie Item Details API URL** with `jwt_token` in the Cookies

      - **_Loader_** will be displayed while fetching the data
      - After the data is fetched successfully,
        - Movie item details received from the response will be displayed
        - Displayed the list of similar movies received from the response
      - If the HTTP GET request made is unsuccessful, then the failure view given in the **Figma** screens will be displayed
        - When the **Try Again** button is clicked, an HTTP GET request will be made to **Movie Item Details API URL**

    - All the header functionalities mentioned in the Home Route will work in this route accordingly
    
</details>


**Search Route**
<details>
<summary>Click to view</summary>
  
  - When an authenticated user opens the Search Route

    - When a value is provided in the search input and the button with the search icon is clicked

      - Will make an HTTP GET request to the **Search Movies API URL**  with `jwt_token` in the Cookies and query parameter `search` with value as the text provided in the search input
      - **_Loader_** will be displayed while fetching the data
      - After the data is fetched successfully, will display the list of movies received from the response
      - If the HTTP GET request made is unsuccessful, then the failure view given in the **Figma** screens will be displayed
        - When the **Try Again** button is clicked, an HTTP GET request will be made to **Search Movies API URL**
      - When the HTTP GET request made to the **Search Movies API URL** returns an empty list for movies then **Search no results** view will be displayed

    - When a **Movie** item is clicked, then the page will be navigated to the Movie Item Details Route
    - All the header functionalities mentioned in the Home Route will work in this route accordingly

</details>


**Account Route**
<details>
<summary>Click to view</summary>
  
  - When an authenticated user opens the Account Route

    - The username which was provided in the login, will be displayed
    - The password which was provided in the login, will be displayed in masked
    - When the **Logout** button is clicked, then the page will be navigated to the Login Route

  - All the header functionalities mentioned in the Home Route will work in this route accordingly

</details>


**Not Found Route**
<details>
<summary>Click to view</summary>
  
  - When a random path is provided as the URL, then the page will navigate to the Not Found Route

</details>

- Users will be able to view the website responsively in mobile view, tablet view as well

### Stretch Goals

<details>
<summary>Additional Functionality added</summary>

- Home Route
  - An HTTP Get request will be made to **Top Rated Movies API URL** as well
    - **_Loader_** will be displayed while fetching the data
    - After the data is successfully fetched from the API
      - Displayed the list of movies received from the top rated movies response
    - If the HTTP GET request made is unsuccessful, then the failure view given in the **Figma** screens will be displayed
      - When the **Try Again** button is clicked, then the HTTP GET request will be made to **Top Rated Movies API URL**
- Users can browse popular movies & searched movies using **_pagination_** buttons.
</details>

## Technologies Used
- React JS
- Figma (for UI/UX design)
- React Slick (for carousel)
- date-fns (for date formatting)
- js-cookies (for handling cookies)
- react-icons (for icons)
- react-router-dom (for routing)
- react-loader-spinner (for loading spinner)
- React (for component management)
- JSX (for component rendering)
- Babel (for transpiling code)
- ESLint (for linting)
- Prettier (for code formatting)
- Webpack (for bundling and asset management)

## Built With
- React JS
- JavaScript
- HTML/CSS
- Figma


### User Credentials

<details>
<summary>Click to view user credentials</summary>

<br/>

**You can use any one of the following credentials**

```text
  username: aakash
  password: sky@007
```

```text
  username: agastya
  password: myth#789
```

```text
  username: advika
  password: world@5
```

<br/>
</details>

### Resources

<details>
<summary>Data fetch URLs</summary>

- **Note:** Use the below sample code snippet to make a POST request on Login using valid username and password.

  ```js
  const options = {
    method: 'POST',
    body: JSON.stringify(userDetails),
  }
  ```

**Login API**

#### API: `https://apis.ccbp.in/login`

#### Method: `POST`

#### Description:

Returns a response based on the credentials provided

#### Sample request object:

```json
{
  "username": "rahul",
  "password": "rahul@2021"
}
```

#### Sample Success Response

```json
{
  "jwt_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJhaHVsIiwicm9sZSI6IlBSSU1FX1VTRVIiLCJpYXQiOjE2MTk2Mjg2MTN9. nZDlFsnSWArLKKeF0QbmdVfLgzUbx1BGJsqa2kc_21Y"
}
```

#### Sample Failure Response

```json
{
  "status_code": 404,
  "error_msg": "Username is not found"
}
```

**Trending Now Movies API**

#### API: `https://apis.ccbp.in/movies-app/trending-movies`

#### Method: `GET`

#### Description:

Returns a response containing the list of all movies

#### Sample Response

```json
{
  "results": [
    {
      "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/no-time-to-die-movie-background-v0.png",
      "id": "92c2cde7-d740-443d-8929-010b46cb0305",
      "overview": "Bond has left active service and is enjoying a tranquil life in Jamaica. His peace is short-lived when his old friend Felix Leiter from the CIA turns up asking for help. The mission to rescue a kidnapped scientist turns out to be far more treacherous than expected, leading Bond onto the trail of a mysterious villain armed with dangerous new technology.",
      "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/no-time-to-die-movie-poster.png",
      "title": "No Time to Die"
    },
    ...
  ],
  "total": 10
}
```

**Top Rated Movies API**

#### API: `https://apis.ccbp.in/movies-app/top-rated-movies`

#### Method: `GET`

#### Description:

Returns a response containing the list of all movies

#### Sample Response

```json
{
  "results": [
    {
      "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/ghostbusters-afterlife-british-movie-background-v0.png",
      "id": "ef6b65e0-3fbf-4ad7-ae0e-25a478648e69",
      "overview": "Ghostbusters: Afterlife is a 2021 American supernatural comedy film directed by Jason Reitman, who co-wrote the screenplay with Gil Kenan.",
      "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/ghostbusters-afterlife-british-movie-poster.png",
      "title": "Ghostbusters: Afterlife"
    },
    ...
  ],
  "total": 10
}
```

**Originals API**

#### API: `https://apis.ccbp.in/movies-app/originals`

#### Method: `GET`

#### Description:

Returns a response containing the list of all movies

#### Sample Response

```json
{
  "results": [
    {
      "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/grindhouse-movie-background-v0.png",
      "id": "efb33428-5527-44d0-a713-1aeef4d56968",
      "overview": "Austin's hottest DJ, Jungle Julia, sets out into the night to unwind with her two friends Shanna and Arlene. Covertly tracking their moves is Stuntman Mike, a scarred rebel leering from behind the wheel of his muscle car, revving just feet away.",
      "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/grindhouse-movie-poster.png",
      "title": "Death Proof"
    },
    ...
  ],
  "total": 10
}
```

**Popular Movies API**

#### API: `https://apis.ccbp.in/movies-app/popular-movies`

#### Method: `GET`

#### Description:

Returns a response containing the list of all movies

#### Sample Response

```json
{
  "results": [
    {
      "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/venom-movie-background-v0.png",
      "id": "320dee56-fdb2-40cf-8df8-92b251bd781f",
      "overview": "Investigative journalist Eddie Brock attempts a comeback following a scandal, but accidentally becomes the host of Venom, a violent, super powerful alien symbiote.",
      "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/venom-movie-poster.png",
      "title": "Venom"
    },
    ...
  ],
  "total": 10
}
```

**Movie Item Details API**

#### API: `https://apis.ccbp.in/movies-app/movies/{movieId}`

#### Example: `https://apis.ccbp.in/movies-app/movies/92c2cde7-d740-443d-8929-010b46cb0305`

#### Method: `GET`

#### Description:

Returns a response containing the details of the movie

#### Sample Response

```json
{
  "movie_details": {
    "adult": false,
    "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/venom-let-there-be-carnage-movie-background-v0.png",
    "budget": "11 Crores",
    "genres": [
      {
        "id": "af2384dc-494b-48a7-a94d-91e6b279f20b",
        "name": "Science Fiction"
      },
      {
        "id": "16106068-2d4e-438f-8a9a-fa0b91e4246a",
        "name": "Action"
      },
      {
        "id": "0c29016b-ff7f-4d67-8f95-f8681bc7ff1c",
        "name": "Adventure"
      }
    ],
    "id": "51b4602f-b0f2-4c81-98e0-a2a409b13926",
    "overview": "Supervillains Harley Quinn, Bloodsport, Peacemaker and a collection of nutty cons at Belle Reve prison join the super-secret, super-shady Task Force X as they are dropped off at the remote, enemy-infused island of Corto Maltese.",
    "poster_path": "/rjkmN1dniUHVYAtwuV3Tji7FsDO.jpg",
    "release_date": "2021-09-30",
    "runtime": 97,
    "similar_movies": [
      {
        "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/dune-movie-background-v0.png",
        "id": "c6ef2389-078a-4117-b2dd-1dee027e5e8e",
        "overview": "Paul Atreides, a brilliant and gifted young man born into a great destiny beyond his understanding, must travel to the most dangerous planet in the universe to ensure the future of his family and his people.",
        "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/dune-movie-poster.png",
        "title": "Dune"
      },
      {
        "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/no-time-to-die-movie-background-v0.png",
        "id": "92c2cde7-d740-443d-8929-010b46cb0305",
        "overview": "Bond has left active service and is enjoying a tranquil life in Jamaica. His peace is short-lived when his old friend Felix Leiter from the CIA turns up asking for help. The mission to rescue a kidnapped scientist turns out to be far more treacherous than expected, leading Bond onto the trail of a mysterious villain armed with dangerous new technology.",
        "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/no-time-to-die-movie-poster.png",
        "title": "No Time to Die"
      },
      {
        "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/shang-chi-and-the-legend-of-the-ten-rings-movie-background-v0.png",
        "id": "046084e1-a782-4086-b723-f98c5c57ebc0",
        "overview": "Shang-Chi must confront the past he thought he left behind when he is drawn into the web of the mysterious Ten Rings organization.",
        "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/shang-chi-and-the-legend-of-the-ten-rings-movie-poster.png",
        "title": "Shang-Chi and the Legend of the Ten Rings"
      },
      {
        "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/grindhouse-movie-background-v0.png",
        "id": "efb33428-5527-44d0-a713-1aeef4d56968",
        "overview": "Austin's hottest DJ, Jungle Julia, sets out into the night to unwind with her two friends Shanna and Arlene. Covertly tracking their moves is Stuntman Mike, a scarred rebel leering from behind the wheel of his muscle car, revving just feet away.",
        "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/grindhouse-movie-poster.png",
        "title": "Death Proof"
      }
    ],
    "spoken_languages": [
      {
        "id": "4bc5f2cf-04d6-4064-bd0d-fc927fda507d",
        "english_name": "English"
      }
    ],
    "title": "Venom: Let There Be Carnage",
    "vote_average": 6.8,
    "vote_count": 1514
  }
}
```

**Search Movies API**

#### API: `https://apis.ccbp.in/movies-app/movies-search?search={searchText}`

#### Example: `https://apis.ccbp.in/movies-app/movies-search?search=Venom`

#### Method: `GET`

#### Description:

Returns a response containing the list of movies and their movie names should includes the given searchText

#### Sample Response

```json
{
  "results": [
    {
      "backdrop_path": "https://assets.ccbp.in/frontend/react-js/movies-app/venom-let-there-be-carnage-movie-background-v0.png",
      "id": "51b4602f-b0f2-4c81-98e0-a2a409b13926",
      "overview": "After finding a host body in investigative reporter Eddie Brock, the alien symbiote must face a new enemy, Carnage, the alter ego of serial killer Cletus Kasady.",
      "poster_path": "https://assets.ccbp.in/frontend/react-js/movies-app/venom-let-there-be-carnage-movie-poster.png",
      "title": "Venom: Let There Be Carnage"
    },
    ...
  ],
  "total": 10
}
```

</details>




