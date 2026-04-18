# ✈️ Frequent Flyers, Infrequent Feelings
*Loyalty and satisfaction are not the same flight. The data has opinions.*

---

## The Hook

I am, unashamedly, an airport person. I arrive two hours early on 
principle. I have opinions about terminal food. I find the chaos 
of departure boards oddly comforting. I hate the middle seat with 
a personal intensity that no loyalty tier has ever compensated for. 
I do not, however, mind the crying baby. That baby is going 
somewhere. We respect the journey.

And yet. Loyalty programs have a funny way of making their most 
loyal customers feel like the least important ones. The points 
accumulate. The tier status climbs. The emails arrive addressed 
to "valued member" with the warmth of an automated system that 
has never once been on a delayed flight at 11 pm with a dead phone 
and a gate change. The experience and the promise keep a polite 
distance from each other.

This project uses 129,880 passenger records to get inside that 
gap. Not to drag airlines  genuinely, I am rooting for them, 
but to find out what actually drives loyalty versus what airlines 
think drives it. Because someone had to put a Random Forest model 
on the loyalty question. It might as well be the girl who still 
gets excited at departure boards.

---

## What Makes This Different

- Are loyal customers actually happy — or just too deep into the points system to leave?
- Of the fourteen service touchpoints an airline measures, which ones actually predict satisfaction and which ones are just on a checklist nobody reads?
- Does loyalty mean the same thing in Business class as it does in Economy — or is the programme doing completely different jobs in different cabins?
- What is the measurable gap between loyal customers who stayed happy and the 38.4% who didn't but kept flying anyway?
- Can a model predict passenger dissatisfaction before the plane lands — and what would an airline do with that information?

---

## Key Findings

1. **38.4% of loyal customers are dissatisfied.** They are still flying. They have not left yet. They are one bad in-flight entertainment system away from a competitor's welcome email.

2. **It is not the wifi. It is not the delays. It is the entertainment.** In-flight entertainment scored 0.263 feature importance, more than double the next closest touchpoint. The screen is doing more work for customer satisfaction than the entire loyalty programme infrastructure.

3. **Loyalty works in Business. In the economy, it is basically decorative.** Business loyal customers sit at 76.4% satisfied. Economy loyal customers sit at 47.0%. That 29 point gap exists between two people with the same tier status on the same airline.

4. **The biggest gap between happy and unhappy loyal customers is entertainment (+1.37) and ease of online booking (+1.29).** The experience starts before the plane. The booking interface is losing people before they even board.

5. **94.2% model accuracy. The data knew before they landed.** A passenger rating inflight entertainment two out of five halfway through a long haul flight is a passenger who is going to land dissatisfied. That is not a mystery. That is a data point with a predictable consequence.

---

## What An Airline Product Team Should Do With This

**Loyalty & Retention —** The 38.4% dissatisfied loyal customer figure is not a rounding error it is a retention crisis in slow motion. Loyal customers who are unhappy are not retained customers. They are delayed departures. The priority should be identifying dissatisfied loyal customers before they reach the competitor's sign-up page, not after.

**In-Flight Product —** Inflight entertainment is the single highest-impact touchpoint in this dataset. An airline investing heavily in points infrastructure while running a mediocre content library is solving the wrong problem. The screen matters more than the tier. That is uncomfortable but the feature importance chart is clear.

**Digital & Booking Experience —** Ease of online booking ranked third in feature importance and second in the gap analysis between satisfied and dissatisfied loyal customers. The loyalty experience starts at the booking interface. A frustrating booking process sets the emotional tone for the entire journey before the passenger has left the house.

**Economy Class Strategy —** An Economy frequent flyer at 47% satisfied is loyal to the schedule, not the airline. The loyalty programme is not doing meaningful retention work in Economy. Either the programme needs to deliver more tangible value to Economy passengers or the product team needs to accept that Economy retention is driven by route availability and price — and invest accordingly.

---

## Project Structure

```
frequent-flyers-infrequent-feelings/
│
├── frequent_flyers_analysis.ipynb      # Full annotated notebook
│
├── chart1_loyalty_illusion             # Satisfaction by customer type
├── chart2_touchpoint_truth             # Random Forest feature importance
├── chart3_class_divide                 # Satisfaction by class and loyalty
├── chart4_breaking_point               # Gap analysis — happy vs unhappy loyal
└── chart5_prediction_model             # Confusion matrix — 94.2% accuracy
│
│   All charts saved as .png and interactive .html
```

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core analysis |
| pandas + NumPy | Data cleaning and manipulation |
| scikit-learn | Random Forest classification, train/test split, feature importance |
| Plotly | Interactive charts |
| Seaborn | Statistical visualisation |

---

## Data Source

**[Invistico Airline Passenger Satisfaction](https://www.kaggle.com/datasets/sjleshrac/airlines-customer-satisfaction)**
129,880 passenger records across 23 variables, including satisfaction 
status, customer loyalty type, cabin class, travel purpose, and 
ratings across fourteen service touchpoints. Chosen because it 
captures the full passenger experience from booking to landing  
not just the flight itself. The fourteen touchpoints are specific 
enough to build a meaningful feature importance model and broad 
enough to tell a complete story about where loyalty actually comes 
from.

---

## What I Learned

The most surprising finding wasn't in the charts — it was in the 
cleaning stage. 38.4% of loyal customers in this dataset are 
dissatisfied. That number sat in the data quality check output 
and I had to look at it twice. Loyal and dissatisfied in the same 
row. Kept flying anyway. That tension is the whole project.

The Random Forest model was the most technically satisfying part 
of this analysis. 94.2% accuracy on a real-world dataset with 
eighteen features is not something you take for granted; it means 
the touchpoints in this dataset are genuinely predictive of 
satisfaction, not just correlated with it. The feature importance 
output was also the most commercially useful thing this project 
produced. In-flight entertainment at 0.263 importance is a finding 
an airline product team can actually do something with.

The class divide finding was the most uncomfortable. I expected 
Business class passengers to be more satisfied, that is obvious. 
I did not expect the economy's loyal customer satisfaction rate to 
be barely higher than chance. 47.0% satisfied with loyalty status 
is not a loyalty programme working. It is a loyalty programme 
that exists. There is a difference, and the slope chart makes it 
visible.

The 594 passengers the model got wrong,  the dissatisfied ones it 
predicted would be satisfied, are the most interesting data points 
in the entire analysis. These are the quiet ones. The passengers 
who rated everything adequately showed no obvious distress signals, 
and were still left unhappy. No model catches everyone. But knowing 
where the blind spots are is half the work.

---

## About

**Trupthi Raj** — Data Analyst 

[GitHub](https://github.com/trupthiraj) · 
[Tableau](https://public.tableau.com/app/profile/trupthi.raj/vizzes)
