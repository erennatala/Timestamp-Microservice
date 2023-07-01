# Date Timestamp Microservice

This is a simple API microservice that takes a date string as a parameter and returns both the Unix timestamp and the UTC string format of the date. It was built with Node.js and Express.js.

## Features

- If no date string is provided, the current date and time is used.
- Accepts date strings that can be successfully parsed by JavaScript's `new Date(date_string)` function.
- Accepts Unix timestamps and returns them as both Unix timestamps and UTC strings.
- If the date string is invalid, the API returns `{ error : "Invalid Date" }`.
- Handles empty date parameters and returns the current time in a JSON object with a `unix` key for the Unix timestamp and a `utc` key for the UTC string.

## Endpoints

`GET /api/:date?`

- If no date is provided, it uses the current date.
- If a Unix timestamp is provided, it parses it as such.
- If a string date is provided, it tries to parse it.
- If the date is invalid (i.e., it couldn't be parsed), it returns `{error: "Invalid Date"}`.
- If the date is valid, it returns an object with the Unix timestamp (`unix`) and the string format of the date (`utc`).

## Example Usage

- `GET /api/1451001600000`
- `GET /api/`

## Example Output

```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

## Running the Project Locally

First, clone the repository:

```bash
git clone https://github.com/<your-github-username>/<repository-name>.git
```

Then, navigate to the project directory and install the dependencies:

```bash
cd <repository-name>
npm install
```

Start the server:

```bash
npm start
```

Open your web browser and navigate to `http://localhost:3000` to start using the application.

## Dependencies

- [Node.js](https://nodejs.org/)
- [Express.js](https://expressjs.com/)
- [CORS](https://www.npmjs.com/package/cors)
```

You can replace `<your-github-username>` and `<repository-name>` with your actual GitHub username and repository name.
