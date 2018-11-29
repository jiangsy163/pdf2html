Define some samples labels for the ground truth and the predicted output:

```

# Define sample labels
true_labels = [2, 0, 0, 2, 4, 4, 1, 0, 3, 3, 3]<br/>
pred_labels = [2, 1, 0, 2, 4, 3, 1, 0, 1, 3, 3]<br/>


```

<br/>Create the confusion matrix using the labels we just defined:

```

\# Create confusion matrix<br/>
confusion_mat = confusion_matrix(true_labels, pred_labels)<br/>


```

<br/></span><span style="font-family: MPDFAA+PalatinoLinotype-Roman; font-size:9px">Visualize the confusion matrix:

```

\# Visualize confusion matrix<br/>
plt.imshow(confusion_mat, interpolation='nearest', cmap=plt.cm.gray)<br/>
plt.title('Confusion matrix')<br/>
plt.colorbar()<br/>
ticks = np.arange(5)<br/>
plt.xticks(ticks, ticks)<br/>
plt.yticks(ticks, ticks)<br/>
plt.ylabel('True labels')<br/>
plt.xlabel('Predicted labels')<br/>
plt.show()<br/>


```

<br/>In the above visualization code, the </span><span style="font-family: MPDFAA+FreeMono; font-size:6px">ticks<br/></span><span style="font-family: MPDFAA+PalatinoLinotype-Roman; font-size:9px"> variable refers to the number of distinct classes.<br/>In our case, we have five distinct labels.<br/>Let's print the classification report:

```

\# Classification report<br/>
targets = ['Class-0', 'Class-1', 'Class-2', 'Class-3', 'Class-4']<br/>
print('\n', classification_report(true_labels, pred_labels,<br/>
target_names=targets))<br/>


```



```

[ 47 ]<br/>


```
