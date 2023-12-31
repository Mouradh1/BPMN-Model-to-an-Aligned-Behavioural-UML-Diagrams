# BPMN-Model-to-an-Aligned-Behavioural-UML-Diagrams


.Transformation rules<hr>
   R1: For each lane whose label is a synonym to "person", "agent" or "system", the corresponding actor name will be the lane name. For each pool/lane whose label is a metonymy of "department", "unit", "division" or "management", the corresponding actor name will be the concatenation of the pool/lane name and the word “Agent” (khlif et al., 2018).
   <br> R2: For each pool:
    <br>R2.1: If the pool includes only business workers (representing the system), set of lifelines and an activation zone representing GUI, entities and control classes that belong to the system perimeter. The classes names follow the linguistic patterns presented above. They are extrated from the obtained fragments.
   <br> R2.2: If the pool contains only business actors then transform each business actor toa lifeline and an activation zone for the instance of the secondary actor. Apply R1 to rename the actor.
   <br> R3: For each lane representing a business worker: 
       <br> a.	Add an actor corresponding to the lane; apply R1 to rename it
       <br> b.	Add a lifeline and an activation zone for the actor generated by R1.
<br>R4: Transform each data to a“BusinessObjectContr, “BusinessObjectGUI, “BusinessObjectentity”.
<br>R5:For each extended attribute of the data representing a compelx noun 1, add:
  <br>  a.	“BusinessObjectEntity” corresponding to the extended attribute if it represents a compelxe noun 1
  <br>  b.	Add an asynchronous message from the actor representing a lane to the “BusinessObjet controller” of the data.
  <br>  c.	Add a synchronous message from the “BusinessObjectContr” of the data to the “BusinessObjectentity”Of the complex noun. Add a response message.
<br>R6: For each extended attribute of the data representing a compelx noun 1 that depends on another noun 2, apply R5 then :
  <br>  a.	Add “BusinessObjectEntity” corresponding to the compelxe noun 2
  <br>  b.	Add an asynchronous message from “BusinessObjet controller” of the data to“BusinessObjectEntity” corresponding to the complexe noun 2.
