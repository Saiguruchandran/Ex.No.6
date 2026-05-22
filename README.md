# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 22-05-2026
# Register no:212223240143
# Aim:
   Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools
# Title:  Framing Prompts for AI-Assisted Project Coding

## Objective

Learners will understand how to design effective prompts for AI tools to assist in coding tasks related to mini projects and final year projects. The activity focuses on creating prompts that help AI systems:

- Generate Python code for interacting with APIs
- Compare outputs from multiple APIs
- Suggest meaningful insights and recommendations
- Improve coding efficiency and project development
- Automate repetitive programming tasks
- Assist in debugging and data analysis

---

# AI Tools Used

| AI Tool | Purpose |
|---|---|
| ChatGPT | Code generation, explanations, debugging |
| Gemini | API comparison and technical responses |
| Claude | Structured explanations and refinement |

---

# Introduction

AI-assisted coding is transforming modern software development by helping developers write code, debug programs, integrate APIs, and analyze outputs efficiently. Instead of manually writing every line of code, developers can frame effective prompts that guide AI systems to generate accurate and reusable solutions.

Prompt engineering plays a major role in improving:
- Code quality
- Development speed
- Error reduction
- Output analysis
- Technical documentation
- Decision-making processes

Well-designed prompts help AI understand:
- Programming language requirements
- API integration details
- Expected outputs
- Data formats
- Analytical requirements

---

# Explanation

AI-assisted coding helps developers generate code, debug applications, integrate APIs, and analyze outputs efficiently. Instead of directly writing programs, students learn how to frame prompts that guide AI systems to produce accurate and useful coding solutions.

Effective prompts should clearly mention:

- Programming language
- Task requirements
- Input and output format
- API details
- Expected comparison or analysis
- Error handling requirements
- Expected recommendations

---

# Exercise Description

Students must practice creating prompts that guide AI tools to:

1. Generate Python code for interacting with multiple APIs
2. Compare outputs from different APIs and highlight differences
3. Suggest insights or next steps based on generated results
4. Improve response quality using refined prompts
5. Analyze AI-generated code and explanations

---

# Use Case Scenario

## Project Scenario

A student is developing a **Weather Analysis Application** that collects weather information from multiple APIs and compares temperature, humidity, and forecast details.

The student uses AI prompts to:
- Generate Python code
- Compare API outputs
- Analyze weather variations
- Suggest meaningful recommendations
- Improve project development efficiency

---

# Stage 1: Prompt for Python API Integration

## Designed Prompt

```text
Generate Python code using the requests library to fetch weather data from two APIs (OpenWeatherMap and WeatherAPI). Display temperature, humidity, and weather conditions for Chennai city.
```

---

## AI-Generated Response

```python
import requests

city = "Chennai"

api1 = "https://api.openweathermap.org/data/2.5/weather?q=Chennai&appid=YOUR_API_KEY"
response1 = requests.get(api1).json()

print("OpenWeatherMap Data")
print("Temperature:", response1["main"]["temp"])
print("Humidity:", response1["main"]["humidity"])

api2 = "https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=Chennai"
response2 = requests.get(api2).json()

print("\nWeatherAPI Data")
print("Temperature:", response2["current"]["temp_c"])
print("Humidity:", response2["current"]["humidity"])
```

---

## Explanation

The AI generated Python code that:
- Connects to two weather APIs
- Retrieves live weather data
- Displays temperature and humidity values
- Demonstrates API integration using Python
- Uses the `requests` library for API communication

---

# Stage 2: Prompt for Comparing API Outputs

## Designed Prompt

```text
Write Python code to compare temperature values returned by OpenWeatherMap and WeatherAPI and display the difference.
```

---

## AI-Generated Response

```python
temp1 = response1["main"]["temp"]
temp2 = response2["current"]["temp_c"]

difference = abs(temp1 - temp2)

print("Temperature Difference:", difference)
```

---

## Explanation

The AI-generated code:
- Extracts temperature values from both APIs
- Calculates the absolute temperature difference
- Displays comparison results clearly
- Helps identify data inconsistencies
- Demonstrates analytical processing using Python

---

# Stage 3: Prompt for Insights and Recommendations

## Designed Prompt

```text
Analyze the compared weather API outputs and suggest meaningful insights if temperature differences are greater than 3 degrees.
```

---

## AI-Generated Response

```python
if difference > 3:
    print("Significant variation detected between APIs.")
    print("Recommendation: Verify data source reliability.")
else:
    print("Weather data from both APIs is consistent.")
```

---

## Explanation

The AI-generated logic:
- Analyzes compared API outputs
- Detects significant variations
- Provides meaningful recommendations
- Demonstrates intelligent decision-making
- Helps improve project analysis

---

# Final Integrated Python Code

```python
import requests

# -------------------------------
# WEATHER API INTEGRATION PROJECT
# -------------------------------

city = "Chennai"

# Replace with your actual API keys
OPENWEATHER_API_KEY = "YOUR_OPENWEATHER_API_KEY"
WEATHERAPI_KEY = "YOUR_WEATHERAPI_KEY"

# -------------------------------
# FETCH DATA FROM OPENWEATHERMAP
# -------------------------------

openweather_url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={OPENWEATHER_API_KEY}&units=metric"

response1 = requests.get(openweather_url)

if response1.status_code == 200:
    data1 = response1.json()

    temp1 = data1["main"]["temp"]
    humidity1 = data1["main"]["humidity"]
    condition1 = data1["weather"][0]["description"]

    print("OpenWeatherMap Data")
    print("--------------------")
    print("Temperature:", temp1, "°C")
    print("Humidity:", humidity1, "%")
    print("Condition:", condition1)

else:
    print("Error fetching OpenWeatherMap data")

# -------------------------------
# FETCH DATA FROM WEATHERAPI
# -------------------------------

weatherapi_url = f"https://api.weatherapi.com/v1/current.json?key={WEATHERAPI_KEY}&q={city}"

response2 = requests.get(weatherapi_url)

if response2.status_code == 200:
    data2 = response2.json()

    temp2 = data2["current"]["temp_c"]
    humidity2 = data2["current"]["humidity"]
    condition2 = data2["current"]["condition"]["text"]

    print("\nWeatherAPI Data")
    print("--------------------")
    print("Temperature:", temp2, "°C")
    print("Humidity:", humidity2, "%")
    print("Condition:", condition2)

else:
    print("Error fetching WeatherAPI data")

# -------------------------------
# COMPARE OUTPUTS
# -------------------------------

difference = abs(temp1 - temp2)

print("\nTemperature Comparison")
print("----------------------")
print("Temperature Difference:", difference, "°C")

# -------------------------------
# INSIGHTS AND RECOMMENDATIONS
# -------------------------------

print("\nInsights")
print("----------------------")

if difference > 3:
    print("Significant variation detected between APIs.")
    print("Recommendation: Verify API reliability or check update timings.")
else:
    print("Weather data from both APIs is mostly consistent.")

# -------------------------------
# FINAL SUMMARY
# -------------------------------

print("\nFinal Summary")
print("----------------------")
print(f"City: {city}")
print(f"OpenWeatherMap Temp: {temp1} °C")
print(f"WeatherAPI Temp: {temp2} °C")
print(f"Temperature Difference: {difference} °C")
```

---

# Prompt Analysis

## Effective Prompt Characteristics

| Feature | Observation |
|---|---|
| Clarity | Clearly specified task requirements |
| Context | Included API names and output requirements |
| Technical Accuracy | AI generated valid Python syntax |
| Readability | Code was simple and understandable |
| Usefulness | Responses were directly applicable to projects |
| Scalability | Code can be extended for larger systems |

---

# Comparative Evaluation

| Stage | Prompt Quality | AI Response Quality | Accuracy | Practical Use |
|---|---|---|---|---|
| API Integration | High | High | High | Excellent |
| Output Comparison | High | High | High | Excellent |
| Insight Generation | Moderate | Good | Good | Very Useful |

---

# Reflection Note

The prompts designed for AI-assisted coding were effective because they clearly described the programming language, APIs, and expected outputs. Detailed prompts helped the AI generate accurate and reusable Python code.

The comparison prompts improved analytical capabilities by helping identify differences between API outputs. Insight-generation prompts demonstrated how AI can assist in decision-making and recommendations.

The prompts could be refined further by:
- Specifying exception handling requirements
- Adding database integration instructions
- Requesting visualization graphs for output comparison
- Including performance optimization requirements
- Asking for modular code structure
- Adding logging and debugging support

---

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/8fcaa3cc-cd94-42f1-8f76-2de8e8c79f3b" />


# Advantages of AI-Assisted Coding

- Faster code generation
- Reduced development time
- Improved productivity
- Better debugging support
- Easier API integration
- Enhanced project analysis
- Helpful for beginners and students

---

# Applications

AI-assisted coding can be applied in:
- Web Development
- Data Science
- Machine Learning Projects
- IoT Applications
- Automation Systems
- API Integration Projects
- Academic Research
- Software Testing

---

# AI-Assisted Coding Workflow

1. Define project requirements  
2. Design effective prompts  
3. Generate AI-assisted code  
4. Compare outputs and results  
5. Analyze insights and recommendations  
6. Refine prompts for better accuracy  
7. Integrate generated solutions into projects  

---

# Findings

1. Prompt refinement significantly improves AI-generated code quality.  
2. Clear instructions help AI produce accurate outputs.  
3. AI-assisted coding reduces manual programming effort.  
4. API comparison prompts improve analytical capabilities.  
5. Insight-generation prompts enhance decision-making support.  
6. Structured prompts improve readability and maintainability.  
7. AI tools are highly useful for academic and real-world projects.  

---

# Conclusion

The experiment demonstrated how prompt engineering can effectively guide AI tools in software development tasks such as API integration, output comparison, and insight generation. Carefully framed prompts improve the accuracy, usefulness, and efficiency of AI-generated code, making AI-assisted coding highly beneficial for academic and real-world projects.

Among the evaluated tasks:
- API integration prompts generated accurate Python code
- Comparison prompts improved analytical processing
- Insight prompts helped generate meaningful recommendations

Overall, effective prompt engineering improves coding productivity, software quality, and project development efficiency.

---

# Result

The prompts for AI-assisted project coding were designed and executed successfully. The AI-generated responses produced functional Python code, output comparisons, and meaningful insights for the project scenario.

The corresponding prompts were executed successfully and demonstrated the effectiveness of AI-assisted coding techniques in software development workflows.
