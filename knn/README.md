# K Nearest Neighbours Algorithm

## Example
Find the k-nearest neighbours, with k=4 for the entire *iris* dataset.
```
data =: 4 readCSV_jLearnUtil_ '/path/to/iris.csv'
knn=: (data,4;(>{.data)) conew 'KNN'
predict__knn ''
┌───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────┬───────...
│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐│┌─────┐...
││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│││0 0 1│...
│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤│├─────┤...
││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │││4    │...
│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘│└─────┘...
└───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────┴───────...
```

Now plot the classes against the first two dimensions of the dataset.
```
R=: I.&:> (~. ="0 _ ])#.&:> maxClasses__knn
pd 'reset'
pd 'type marker'
pd <"2 (<"1 |:2{."1 >{.data) ({~&:>)"0 _ <"1 R
pd 'show'
```
Results for `k=2,4,6`:

![knn2](/knn/knn_2neighbours.png)
![knn4](/knn/knn_4neighbours.png)
![knn6](/knn/knn_6neighbours.png)