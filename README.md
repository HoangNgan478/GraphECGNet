# GraphECGNet

### **In this respect, our paper has the following contributions:**

- **A practical approach to detect edges of waveform in ECG images, using the Sobel operator.**

- **A workable solution to the classification of heart diseases, deploying GNN techniques on ECG signals. To the best of our knowledge, our study is the first attempt to deploy GNNs in automatically classifying ECG signals for detecting heart problems.**

- **An empirical evaluation on the two real ECG datasets to compare our proposed model with two state-of-the-art approaches using convolutional neural networks (ResNet26D and ConvNet).**


### File Structure and Working procedure
```
1. Fist, convert ECG signals from PTB-XL database to images using signal2image.py
2. Then, apply edge detection accroding to the class-number: edge_transformation.py
3. Afterwards, prepare graph-datasets using edge-preparation: Graph_construction.py
4. Finally edge preperation produces five kinds of dataset for graph classification:
  path name: .../GraphTrain/dataset/<dataset_name>/raw/<dataset_name>_<data_file>.txt. 
  <data_file> can be:
    
    4.1. A--> adjancency matrix 
    
    4.2. graph_indicator--> graph-ids of all node 
    
    4.3. graph_labels--> labels for all graph 
    
    4.4. node_attributes--> attribute(s) for all node 
    
    5.5. node_labels--> labels for all node
    
5. After all the graph datasets are created properly, run main.py. The graph datasets are loaded through dataloader.py and the model is called through model.py
```
