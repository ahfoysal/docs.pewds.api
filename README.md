<h1 align="center"> Pewds Api </h1>

Welcome to the documentation for Pewds Api - a collection of high-level, search engine APIs that provide accurate information about numerous entertainment mediums (such as anime, movies, news etc.), along with links to stream these contents from publicly-available online sources.

**Example** - searching for anime .

```ts
import axios from "axios";

// Using the example query "one piece", and looking at the first page of results.
const url = "https://api.pewds.vercel.app/anime/search/one piece";
const data = async () => {
  try {
    const { data } = await axios.get(url, { params: { page: 1, perPage: 40 } });
    return data;
  } catch (err) {
    throw new Error(err.message);
  }
};

console.log(data);
```

Do you want to know more? Head to the [`Getting Started`](https://docs.pewds.vercel.app/rest-api/start).
