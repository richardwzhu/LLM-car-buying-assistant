# LLM Powered Car-Buying Assistant

With over 40 automotive brands sold in the US, the car market is a dynamic landscape. Individuals can make informed purchasing decisions by parsing through reviews on the internet, but the process is time-consuming.
This LLM application provides users an immediate analysis of the current best cars at a user specified price point.

## Example Usage (see notebook for code)
Let's assume our user wants to purchase a new EV with $50k. Our query is "What are the best electric cars from 2023 that are around $50k?"

## Without Metaphor API
Inputting this query into an OpenAI LLM, we get:
```
As an AI language model, I don't have real-time information on specific car models from 2023. However, I can provide you with some electric vehicles that were popular in 2022 and may fall within the $50,000 price range. It's important to note that prices can vary depending on specifications, location, and available incentives. Here are a few options:

1. Tesla Model 3: The base model starts at around $40,000, offering good range and performance.
2. Chevrolet Bolt EV: A compact electric car with a starting price around $36,000, providing decent range and features.
3. Nissan Leaf Plus: The Leaf Plus offers an extended range and starts at approximately $40,000.
4. Hyundai Kona Electric: This affordable electric SUV starts around $40,000 and offers competitive range.
5. Ford Mustang Mach-E: Ford's all-electric SUV offers various trims and starts around $43,000 before incentives.

Keep in mind that availability and pricing can change significantly from year to year, so these suggestions may not reflect the market in 2023. It's advisable to check with local dealerships or automotive websites for the latest information on electric car offerings within your price range.
```
The results here are somewhat useful, but the OpenAI model is unable to access real-time information on the latest car models.


## With Metaphor API
We can use Metaphor's neural search engine to better address the user's question.

Leveraging Metaphor's content retrieval API, we can aggregate search results for our query and then use OpenAI's LLM to summarize the results. Compared to the initial results without Metaphor, our program is able to suggest new cars from 2023 and provide exact price points.
```
Based on your query for "Top-rated electric cars 2023 under $50k," here is a
list of new cars that fit your criteria:

1. 2023 Mini Cooper Electric: This go-kart-like EV has a starting price of ju
st over $30,000 and offers a range of 110 miles. It comes with lots of standa
rd features and provides a fun driving experience.

2. 2023 Nissan Ariya: Nissan's new electric SUV offers up to 304 miles of dri
ving range and has a starting price of $44,485. It features a sporty design,
advanced driver-assistance features, and infotainment technology.

3. 2024 Chevrolet Equinox EV: This compact SUV is expected to have a starting
price of around $30,000 and a range of up to 300 miles. It features a sleek d
esign, a spacious interior, and comes with advanced technology options.

4. 2023 Kia Niro EV: The redesigned Niro EV offers a range of up to 253 miles
and has a starting price that fits within your budget. It comes with a distin
ctive design, recycled materials in the interior, and a 10.3-inch infotainmen
t display.

These are just a few options to consider. It's always a good idea to visit lo
cal dealerships and take test drives to see which car suits your needs and pr
eferences best.
```
