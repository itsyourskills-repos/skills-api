---
sidebar_position: 2
slug: "search-api"
---

# Search API

The Search API in ISOT empowers users to find specific skills by submitting queries. It utilizes a matching process that considers relevant "terms" and returns a list of matched terms along with associated skills. This enables users to efficiently discover skills based on their search queries.

![Search Skills](https://i.imgur.com/P9aJbTl.png)

_Above is a screenshot illustrating how skills can be searched._

## API Request

To perform a skill search, make a GET request to the API with the desired query. Here is an example using cURL:

```bash
curl --request GET \
	--url 'https://iys-skill-api.p.rapidapi.com/?q=aws&limit=10' \
	--header 'X-RapidAPI-Host: iys-skill-api.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: <YOUR-API-KEY>'
```

Ensure to replace `<YOUR-API-KEY>` with your actual Rapid API Key.

## API Response

The response is in JSON format and includes the query and a list of matches for the query. Example response:

```json
{
  "query": "Java",
  "matches": [
    {
      "term": "Java",
      "skills": [
        {"path_addr": "100.101", "name": "Java programming", ...}, // Under Mobile App Development
        {"path_addr": "150.101", "name": "Java programming", ...}, // Under Server Applications
        {"path_addr": "160.102", "name": "Java tutoring", ...}
      ]
    },
    {
      "term": "JavaScript",
      "skills": [
        {"path_addr": "200.201", "name": "JavaScript programming", ...}
      ]
    }
  ]
}
```

## Mapping Skills to Terms

To facilitate matching, each skill is mapped to one or more terms. For example, the skill "JavaScript programming" is mapped to the terms "JavaScript" and "JS." The API matches these terms with user queries, returning the relevant skills.

## Example Use Case

If a user searches for "Java," the API matches the query with terms like "Java" and "JavaScript," returning associated skills. In the example response, "Java programming" appears twice under different categories (Mobile App Development and Server Applications).

## Note

- Use the `path_addr` as an identifier for the selected skill path, especially when interacting with other APIs, such as retrieving children of a skill.
- Implement dropdown lists of skills using terms from the "matches" array for user-friendly search options.

Explore the Search API to enhance your skill discovery experience within the ISOT database. For further assistance or inquiries, refer to the API documentation or reach out to our support team.