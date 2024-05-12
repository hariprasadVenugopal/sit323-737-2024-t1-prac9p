<b>SIT323/SIT737- Cloud Native Application Development</b>

<b>9.1P: Adding a database to your application</b>

<ul>
      <li>Clone the repository.</li>
      <li>Run the command <b>kubectl apply -f .\createStorageClass.yaml</b></li>
      <li>Run the command <b>kubectl apply -f .\createStatefulSet.yaml</b></li>
      <li>Run the command <b>kubectl apply -f .\createConfigMap.yaml</b></li>
      <li>Run the command <b>kubectl apply -f .\createMongoDbSecret.yaml</b></li>
      <li>Run the command <b>kubectl apply -f .\createHeadlessService.yaml</b></li>
      <li>Check the deployment status using this command <b>kubectl get deployments</b></li>
      <li>Check the pods status using this command <b>kubectl get pods</b></li>
      <li>Check the service status using this command <b>kubectl get services</b></li>
      <li>Once the pods are ready try this command <b>kubectl exec -it mongo-0 -- mongo</b></li>
      li>then paste this command in mongo shell<b>rs.initiate({
   _id: "rs0",
   members: [
     { _id: 0, host: "mongo-0.mongo.default.svc.cluster.local:27017" },
     { _id: 1, host: "mongo-1.mongo.default.svc.cluster.local:27017" },
     { _id: 2, host: "mongo-2.mongo.default.svc.cluster.local:27017" }
   ]
});</b></li>
      <li>Then open mongo shells for remaining pods and try this command <b>rs.slaveOk</b></li>
      <li>Then try create,update, delete data from the collection in the primary using this <b>insertOne</b>, <b>updateOne</b>, <b>deleteOne</b> commands</li>
</ul>
