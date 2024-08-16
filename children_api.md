---
sidebar_position: 3
slug: "children-api"
---

# Children API

The Children API in ISOT empowers users to retrieve a list of children skills based on a specified skill's `path_addr`. This functionality allows users to explore and understand the hierarchy of skills, providing insights into the subcategories or specific skills related to a particular parent skill.

![Children Skills Display](https://i.ibb.co/17KZbR1/Screenshot-from-2023-04-16-20-23-24.png)

_Above is a screenshot illustrating how children skills are displayed._

## API Request

To retrieve the children of a skill, make a GET request to the API with the desired `path_addr`. Here is an example using cURL:

```bash
curl --request GET \
	--url 'https://iys-skill-api.p.rapidapi.com/children/?path_addr=199.200' \
	--header 'X-RapidAPI-Host: iys-skill-api.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: <YOUR-API-KEY>'
```

Ensure to replace `<YOUR-API-KEY>` with your actual Rapid API Key.

## API Response

The response is in JSON format and includes a list of skills representing the children of the specified skill. Example response:

```json
[
  {
    "path_addr": "199.200.201",
    "name": "JavaScript programming",
    ...
  },
  {
    "path_addr": "199.200.202",
    "name": "HTML coding",
    ...
  },
  {
    "path_addr": "199.200.203",
    "name": "CSS coding",
    ...
  }
]
```

## Example Use Case

Suppose you have the skill "Web Development" with a `path_addr` of "199.200." By querying the Children API with this path, you will receive a list of children skills, such as "JavaScript programming," "HTML coding," and "CSS coding."

## Note

- Utilize the `path_addr` parameter in the API call to specify the skill for which you want to retrieve children.
- The response provides a list of skills representing the immediate children of the specified skill.

Explore the Children API to enhance your skill exploration within the ISOT database. If you have any questions or encounter issues, refer to the API documentation or reach out to our support team for assistance.