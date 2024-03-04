### Hello there, you fellow Legend! ####

My name's Nikola (or Niki), an avid data analyst based in Barcelona, Spain.

If you are in a rush, navigating this profile at the speed of light, here's the usual [LinkedIn stuff](https://www.linkedin.com/in/nikolavlvladimirov/).

But, if you're a fellow Python enthusiast ready to soar to new heights, buckle up and execute this little script below:
            
```python
from dataclasses import dataclass

@dataclass
class MyProfile:
    name: str
    position: str
    location: str
    stack: list
    languages: list
    skills: list
    linkedin_url: str

    def display_summary(self):
        print(self)

    def __str__(self):
        return (
            f"Name: {self.name}\n"
            f"Current Position: {self.position}\n"
            f"Current Location: {self.location}\n"
            f"Stack: {', '.join(self.stack)}\n"
            f"Languages: {', '.join(self.languages)}\n"
            f"Skills: {', '.join(self.skills)}\n"
            f"LinkedIn: {self.linkedin_url}"
        )

# Initialize the profile dictionary
profile_dict = {
    'name': "Nikola Vladimirov",
    'position': "Product Data Analyst",
    'location': "Barcelona, Spain",
    'stack': ["Python", "SQL", "AWS", "Snowflake", "Databricks", "Azure", "PBI", "MS Office"],
    'languages': ["English", "Spanish", "French", "Bulgarian"],
    'skills': ["Project Management (Data-Driven)", "Analytics", "A/B Testing", "Pipeline Optimization", "ETLs"],
    'linkedin_url': "https://www.linkedin.com/in/nikolavlvladimirov/"
}

# You know the drill...
if __name__ == '__main__':
    my_profile = MyProfile(**profile_dict)
    my_profile.display_summary()
