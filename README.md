# Foodie Tour Creator with Julep AI

This project uses Julep AI to create personalized one-day foodie tour recommendations for cities around the world, taking into account current weather conditions, local cuisine, and top restaurants.

## Overview

The Foodie Tour Creator is an intelligent workflow that:

1. Fetches real-time weather data for specified cities
2. Researches iconic local dishes for each city
3. Identifies top-rated restaurants in each location
4. Gathers culinary background information from Wikipedia
5. Generates a detailed, personalized foodie tour itinerary that:
   - Recommends indoor or outdoor dining based on weather
   - Selects 3 iconic local dishes that represent the city's culinary heritage
   - Suggests specific restaurants for each meal
   - Creates a narrative for a one-day tour with breakfast, lunch, and dinner

## Requirements

- Python 3.6+
- Julep client library
- PyYAML
- OpenWeatherMap API key
- Brave Search API key

## Installation

```bash
pip install julep pyyaml -U
```

## Usage

1. Clone this repository
2. Open the `foodie_tour_workflow.ipynb` notebook
3. Run the cells in sequence
4. The results will be saved to `foodie_tour_results.md`

You can modify the list of cities in the execution cell:

```python
cities = ["New York", "Tokyo", "Paris", "Bangkok", "Rome"]
```

## How It Works

The workflow is orchestrated through Julep AI's task system:

1. **Setup**: Initializes the Julep client and creates an agent
2. **Tools Integration**: Configures weather, internet search, and Wikipedia tools
3. **Task Definition**: Defines a YAML workflow with sequential steps
4. **Execution**: Runs the workflow with the specified cities
5. **Results**: Monitors execution and saves the output

### Workflow Steps

1. Fetch current weather data for each city
2. Search for iconic local dishes in each city
3. Find top restaurants in each city
4. Gather culinary information from Wikipedia
5. Combine all data for each city
6. Generate personalized foodie tour recommendations
7. Compile results into a final output

## Sample Output

For each city, the output includes:

- Weather analysis and indoor/outdoor dining recommendations
- Three iconic local dishes with cultural context
- Recommended restaurants for each dish
- A narrative itinerary with timing suggestions
- Additional tips for transportation and dining

Example for Paris:
```
### One-Day Foodie Tour in Paris, France

**Weather Analysis**
Given the current weather conditions in Paris, with moderate rain and a high humidity level, indoor dining is advisable for the day.

**Iconic Local Dishes Selection**
1. **Steak Frites:** A quintessential Parisian dish representing the classic French bistro experience.
2. **Ratatouille:** A traditional Provençal stewed vegetable dish embodying seasonal flavors.
3. **Crepes:** Light, versatile, and indicative of French culinary creativity.

**Tour Itinerary**
...
```

## API Keys

The notebook uses the following API keys:
- OpenWeatherMap API for weather data
- Brave Search API for internet searches

## License

This project is available for personal and educational use.

## Acknowledgments

- Julep AI for providing the agent framework
- OpenWeatherMap for weather data
- Brave Search for search capabilities
- Wikipedia for culinary information
