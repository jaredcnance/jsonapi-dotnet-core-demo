# JsonApiDotNetCore Todo List Example

Demo application for [JsonApiDotNetCore](https://github.com/json-api-dotnet/JsonApiDotNetCore/) using [Ember.js](https://emberjs.com/).

Back in 2017, Jared Nance did an excellent [video series](https://www.youtube.com/watch?v=KAMuo6K7VcE&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf) in which he built this demo:
- [Part 1: Server Setup](https://www.youtube.com/watch?v=KAMuo6K7VcE&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf)
- [Part 2: Client Setup](https://www.youtube.com/watch?v=_d53rG2i9pY&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf&index=2)
- [Part 3: Server Authentication and Authorization](https://www.youtube.com/watch?v=GIQqIz1Gpvo&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf&index=4)
- [Part 4: Client Sessions](https://www.youtube.com/watch?v=CHdoya6rvaA&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf&index=6)
- [Part 5: Persisting Data](https://www.youtube.com/watch?v=bZ1D_aYGJnU&list=PLu4Bq53iqJJAo1RF0TY4Q5qCG7n9AqSZf&index=7)

## Usage

### Start the database

The app requires running postgres instance with credentials specified in appsettings.json.
One way to do this is run the database in a Docker container:

```sh
docker run --name TodoListSampleDb \
    -e POSTGRES_USER=postgres \
    -e POSTGRES_PASSWORD=postgres \
    -e POSTGRES_DB=TodoList \
    -p 5432:5432 \
    -d postgres
```

### Starting the API

- `cd TodoListAPI`
- Set the environment to development: `export ASPNETCORE_ENVIRONMENT=development` (mac)
- `dotnet run`

### Starting the Client

- Install ember-cli:
    `npm install -g ember-cli`

- Install packages:
    `npm install -g yarn`
    `yarn install`

- `ember s` or `yarn start`

- Updating to the latest version of Ember:
    `npm install -g ember-cli-update`
    `ember-cli-update`
    `ember-cli-update --run-codemods`
    `yarn install`

In case you haven't watched the videos: the default username/password is `guest`/`Guest1!`.
