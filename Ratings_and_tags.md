---
sidebar_position: 5
slug: "ratings-and-tags"
---

# Ratings and Tags

Each skill in the ISOT database includes information about ratings and tags, providing valuable insights into the candidate's skill level and additional categorization.

### Ratings

Skills may have various types of ratings to offer a clearer understanding of the candidate's proficiency and experience. For instance, a skill can be rated based on proficiency levels (e.g., Learning, Basic, Advanced, or Expert User), years of experience (e.g., 0-2 years, 2-5 years, 15-10 years, or 10+ years), and recency of experience (e.g., Current or Past).

#### Example Ratings Object

```json
"ratings": [
  {
    "_id": "ratings/1",
    "rating_category": "Experience Recency",
    "rating_scale_type": "Two Choice Rating",
    "rating_scale_label": ["Current", "Past"]
  },
  {
    "_id": "ratings/2",
    "rating_category": "Experience Level",
    "rating_scale_type": "Four Scale Rating",
    "rating_scale_label": ["0-2 years", "2-5 years", "15-10 years", "10+ years"]
  }
]
```

### Tags

Tags serve as additional labels for skills, providing a way to categorize or highlight specific attributes. Each tag is represented as an object.

#### Example Tags Object

```json
"tags": [
  {
    "_key": "4",
    "_id": "tags/4",
    "title": "Occupation"
  }
]
```

## Example Skill Information

```json
{
  "path_addr": "199.200.201",
  "name": "JavaScript programming",
  "ratings": [
    {
      "_id": "ratings/1",
      "rating_category": "Experience Recency",
      "rating_scale_type": "Two Choice Rating",
      "rating_scale_label": ["Current", "Past"]
    },
    {
      "_id": "ratings/2",
      "rating_category": "Experience Level",
      "rating_scale_type": "Four Scale Rating",
      "rating_scale_label": ["0-2 years", "2-5 years", "15-10 years", "10+ years"]
    }
  ],
  "tags": [
    {
      "_key": "4",
      "_id": "tags/4",
      "title": "Occupation"
    }
  ],
  ...
}
```

## Utilizing Ratings and Tags

- **Ratings:** Use the provided `_id` to reference the rating type in your database. The `rating_category` serves as a title for the rating, and `rating_scale_type` guides the type of input widget to display.

- **Tags:** Utilize the `title` attribute to showcase the tag associated with a skill. Tags can be helpful for additional categorization or highlighting specific aspects of a skill.

These attributes contribute to a more comprehensive understanding of a candidate's skills and enhance the versatility of the ISOT database. If you have any questions or require further assistance, feel free to refer to the API documentation or reach out to our support team.