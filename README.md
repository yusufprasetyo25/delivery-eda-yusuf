This is an exploratory data analysis for [this data](https://github.com/indrasetiadhip/data-task-sample).

In the notebook, we explore these topics about the data:
1. We can check if there are any duplicate IDs in the data.
2. According to the `README.md` of the source, the sample data should contain 10 days delivery data. We are going to check if it is really the case.
3. If the delivery data contains full data of the day, we can check for the (most/least) busy day.
4. There are undone tasks in the dataset. If the data is cut at certain cutoff, the undone task should be concentrated on the last days in the dataset. We need to be cautious when analyzing those data. 
5. We can know the rush hour of the origin branch from `taskCreatedTime`. We can improve the experience of the customers and our employees by putting more workers during those critical hours.
6. Since we have the information of the worker, we can check for the worst/best worker (productivity). However, the main problem is we don't know what assigned means. Is the assigned worker related to the delivery location? Is there a worker working for two or more branch?
7. We can investigate `UserVar.branch_dest` and `taskLocationDone` Relationship.
8. There are quite a few `UserVar.taskDetailStatusLabel`. We can check for the failed status and see whether there are any pattern to other columns.
9. We can check whether the `taskLocationDone` is the nearest to the branch destination and suggest new branches that will increase our delivery efficiency.
10. Since we have `UserVar.receiver_city`, we can check whether it correspond to `taskLocationDone`. Cheating workers can set the delivery to failed status far from the place of the customer.
11. We can check for the rush hour of the `taskCompletedTime` to adjust our workers schedule.

Also, I used external data from [opendatasoft](https://data.opendatasoft.com/api/explore/v2.1/catalog/datasets/airports-code@public/exports/json?lang=en&timezone=Asia%2FJakarta) and [Nominatim](https://nominatim.org/)