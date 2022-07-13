### The Locations clustering POC
Locations clustering proof-of-concept test task.

Given that we have a dataset which has around 60k of **location addresses**, including *city*, *road*, *house_number*, *postcode* and *state*: [Download the Locations dataset](https://drive.google.com/file/d/11sPSrssE39CPN73amoFvzosuAJpjyBqG/view?usp=sharing)

The data look like this:
![data](https://user-images.githubusercontent.com/25924/177707968-c6143674-c9ca-4057-8c8a-a565dc7169fd.png)

The candidate is expected to create a solution - a proof of concept, using Python, to cluster (or simply group) those addresses where they belong to the same place (same address). Candidate is free to implement any machine learning model, or hand-crafting solutions to show how the candidate would approach to solve this problem.

For example, these records below could be **scattered** around the orignal locations CSV, and we want to "group" them together into their own cluster, and don't remove the duplicates:

### Example of how the output could look like:
|city        |road           |house_number|postcode  |state         |cluster_id|record_idx|
|-----------:|--------------:|-----------:|---------:|-------------:|---------:|---------:|
|simpsonville|fairview rd    |692         |29680-6708|south carolina|1         |23        |
|simpsonville|fairview rd    |692         |29680     |sc            |1         |434       |
|simpsonville|fairview road  |692         |29680     |sc            |1         |543       |
|simpsonville|fairview rd    |692         |29680     |sc            |1         |34        |
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
|maumee      |arrowhead rd   |1401        |43537     |oh            |3         |275       |

### Instructions:
 - Fork this repo or create a new public GitHub repo for the solution.
 - The solution will open/read the location data CSV file and write the grouped/clustered result in an output CSV file.
 - There's no restriction on how the candidate would choose to approach the problem.

Please email to: long@shake.io if you have any questions.

Good luck!
