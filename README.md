### The Locations clustering POC
Locations clustering proof-of-concept test task.

Given that we have a dataset which has around 60k of **location addresses**, including *city*, *road*, *house_number*, *postcode* and *state*: [Download the Locations dataset](https://drive.google.com/file/d/11sPSrssE39CPN73amoFvzosuAJpjyBqG/view?usp=sharing)

The original locations data look like this:
|city        |road            |house_number|postcode  |state         |
|---------:|-----------------:|-----------:|---------:|-------------:|
|fort worth|sycamore school rd|5421        |76123     |texas         |
|gautier   |highway 90        |2701        |39553     |mississippi   |
|farmington|e main            |4750        |87401     |nm            |
|richland  |queensgate drive  |2751        |99352     |washington    |
|davie     |s state hwy seven |1600        |33317     |fl            |
|crestview |w james lee blvd w|302         |32536     |fl            |
|eufaula   |s eufaula ave     |1250        |36027     |al            |
|mccalla   |eastern valley rd |4746        |35111     |alabama       |
|hugoton   |e 11th st         |612         |67951     |ks            |

The candidate is expected to create a solution - a proof of concept, using Python, to cluster (or simply group) those addresses where they belong to the same place (same address). Candidate is free to implement any machine learning model, or hand-crafting solutions to show how the candidate would approach to solve this problem.

For example, these records below could be **scattered** around the orignal locations CSV, and we want to "group" or "link" them together into their own single address cluster with the same house number on the same road, and don't remove the duplicates. The primary challenge is that some of the entries are written differently than others: e.g. "fairview rd" vs "fairview road", or "south carolina" vs "sc".

### Example of how the an output could look like:
|city        |road           |house_number|postcode  |state         |cluster_id|record_idx|
|-----------:|--------------:|-----------:|---------:|-------------:|---------:|---------:|
|simpsonville|fairview rd    |692         |29680-6708|south carolina|1         |23        |
|simpsonville|fairview rd    |692         |29680     |sc            |1         |434       |
|simpsonville|fairview road  |692         |29680     |sc            |1         |543       |
|simpsonville|fairview rd    |692         |29680     |sc            |1         |25436     |
|simpsonville|fairview rd    |692         |29680     |south carolina|1         |78        |
|hialeah     |e 10th ave     |1021        |33010     |florida       |2         |653       |
|hialeah     |e 10th ave     |1021        |33010     |fl            |2         |24        |
|hialeah     |e 10th avenue  |1021        |33010     |fl            |2         |87        |
|hialeah     |e 10th ave     |1021        |33010     |florida       |2         |4576      |
|maumee      |arrowhead dr   |1401        |43537     |ohio          |3         |987       |
|maumee      |arrowhead drive|1401        |43537     |ohio          |3         |2476      |
|maumee      |arrowhead rd   |1401        |43537     |oh            |3         |2356      |
|maumee      |arrowhead rd   |1401        |43537     |oh            |3         |453       |
|maumee      |arrowhead rd   |1401        |43537     |ohio          |3         |819       |

### Instructions:
 - Fork this repo or create a new public GitHub repo for the solution.
 - The solution will open/read the location data CSV file and write the grouped/clustered result in an output CSV file.
 - There's no restriction on how the candidate would choose to approach the problem.

Please email to: long@shake.io if you have any questions.

Good luck!
