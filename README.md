# hello-world
My first repository in GitHub
# Myself NARAVA SIVA NAGA MALLIK
Customised AI Kitchen in INDIA
Creating a code for a Customized AI Kitchen in India involves integrating various technologies such as IoT (Internet of Things), AI (Artificial Intelligence), and machine learning to automate and optimize kitchen operations. 
This is a basic starting point. Building a full-fledged AI kitchen system would involve integrating various components, ensuring they communicate effectively, and adding user-friendly interfaces.

import openai

openai.api_key = 'your-openai-api-key'

def get_recipe_recommendations(ingredients):
    
    prompt = f"Suggest a recipe based on the following ingredients: {', '.join(ingredients)}"

response = openai.Completion.create(
        
        engine="text-davinci-003",
        
        prompt=prompt,
        
        max_tokens=100
) 

recipe = response.choices[0].text.strip()
    
    return recipe

ingredients = ["tomato", "onion", "ginger", "garlic", "salt", "pepper"] 

recipe = get_recipe_recommendations(ingredients) 

print(f"Recommended Recipe:\n{recipe}")
