---
sidebar_position: 3
slug: "getting-started"
---

# Getting Started

To begin utilizing the ISOT API and accessing the extensive skill database, follow these simple steps:

## 1. Subscribe to ISOT API

Visit [ISOT API on RapidAPI](https://rapidapi.com/iys-skills-tech-iys-skills-tech-default/api/iys-skill-api) and subscribe to the plan that suits your needs. Upon subscription, you will obtain a crucial component for API access - the **Rapid API Key**.

## 2. Acquire the Rapid API Key

Once subscribed, retrieve your unique **Rapid API Key**. This key is essential for authenticating your requests and gaining access to the ISOT skill database.

## 3. Make API Calls

Now that you have your API key, you can start making calls to the ISOT API using tools like `curl`. The example below demonstrates how to retrieve skills related to "aws" with a limit of 10 results:

```shell
curl --request GET \
	--url 'https://iys-skill-api.p.rapidapi.com/?q=aws&limit=10' \
	--header 'X-RapidAPI-Host: iys-skill-api.p.rapidapi.com' \
	--header 'X-RapidAPI-Key: <YOUR-API-KEY>'
```

Ensure to replace `<YOUR-API-KEY>` with the actual Rapid API Key you obtained in the previous step.

## Note

- The `q` parameter in the API call allows you to specify the skill or keyword you are searching for.
- Adjust the `limit` parameter according to your requirements to control the number of results returned.

## Explore and Integrate

Feel free to explore more endpoints and functionalities provided by the ISOT API. Whether you are integrating it into your application, conducting research, or enhancing your skill management system, the ISOT API offers a powerful and versatile solution.

If you encounter any issues or have questions, refer to the API documentation on RapidAPI or contact our support team for assistance.
