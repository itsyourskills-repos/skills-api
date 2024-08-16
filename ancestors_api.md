---
sidebar_position: 4
slug: "ancestors-api"
---

# Ancestors API

The Ancestors API within ISOT allows users to retrieve a hierarchical list of ancestor skills based on a provided `path_addr`. This hierarchical order presents parent skills first, followed by grandparent skills, and so on. These ancestor skills essentially represent categories that help users understand the context and relationships of a particular skill within the broader skill hierarchy.

## API Request

To utilize the Ancestors API, make a GET request with the desired `path_addr`. Here is an example using cURL:

```shell
curl --request GET \
	--url 'https://iys-skill-api.p.rapidapi.com/ancestors/?path_addr=199.200' \
	--header 'X-RapidAPI-Host: iys-skill-api.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: <YOUR-API-KEY>'
```

Ensure to replace `<YOUR-API-KEY>` with your actual Rapid API Key.

## API Response

The response is a JSON array containing skill objects with their `path_addr` and names, representing the ancestors in hierarchical order. Example response:

```json
[
  {
    "path_addr": "199.200",
    "name": "Web Development",
    ...
  },
  {
    "path_addr": "199",
    "name": "Computer Science",
    ...
  }
]
```

## Example Use Case

Consider the skill "JavaScript Programming" with a `path_addr` of "199.200". By querying the Ancestors API with this path, you will receive a list of ancestor skills, such as "Web Development" and "Computer Science."

This API is useful for enabling users to browse through skill categories, gaining insights into the broader context of a specific skill within the ISOT hierarchy.

## Note

- Customize the `path_addr` parameter in the API call to retrieve ancestors for different skills.
- The order of skills in the response reflects the hierarchical relationship, with the immediate parent skill appearing first.

Explore the Ancestors API to enhance your skill exploration and categorization within the ISOT database. If you have any questions or encounter issues, refer to the API documentation or contact our support team for assistance.