+++
title = "Analysis Models"
description = ""
weight = 100
+++

#### Data Flow Diagram
`TODO`

#### Entity-Relationship Diagram (ER Diagram)
`TODO`

#### Dialog Map

<iframe frameborder="0" style="width:100%;height:597px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Dialog%20Map.html#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1PPxpYY9XT-8TiFQFEEy5Drvb61QO1U6r%26export%3Ddownload"></iframe>

#### Decision Tables

<table>
  <tr>
    <td/>
    <td colspan="6">Requirement Number</td>
  </tr>
  <tr>
    <td>Condition</td>
    <td>1</td>
    <td>2</td>
    <td>3</td>
    <td>4</td>
    <td>5</td>
    <td>6</td>
  </tr>
  <tr>
    <td>isOperator</td>
    <td>F</td>
    <td>T</td>
    <td>T</td>
    <td>T</td>
    <td>T</td>
    <td>T</td>
  </tr>
  <tr>
    <td>isAdmin</td>
    <td>-</td>
    <td>F</td>
    <td>F</td>
    <td>F</td>
    <td>T</td>
    <td>T</td>
  </tr>
  <tr>
    <td>isDispatched</td>
    <td>-</td>
    <td>T</td>
    <td>T</td>
    <td>F</td>
    <td>T</td>
    <td>T</td>
  </tr>
  <tr>
    <td>isResolved</td>
    <td>-</td>
    <td>F</td>
    <td>T</td>
    <td>F</td>
    <td>F</td>
    <td>T</td>
  </tr>
  <tr>
    <td>Action</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Accept Dispatch</td>
    <td></td>
    <td></td>
    <td></td>
    <td>X</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Reject Dispatch</td>
    <td>X</td>
    <td>X</td>
    <td>X</td>
    <td></td>
    <td>X</td>
    <td>X</td>
  </tr>
</table>
