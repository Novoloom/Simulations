# Simulations REST API

High fidelity renders of garments. This repository is owned by Milin. Our server is written in Node, and we use ExpressJS. The API should be called from https://novoloom.com/simulations/{NAME_OF_METHOD}.

## POST /rigidGarmentModel
 
Submits mesh data for a rigid 3D model of a garment for simulation. Represented by an array of vertices, and an array of index pair than indicate which vertices are joined by an edge.

### Example 

The HTTP request below submits a square made of 2 triangles to be simulated as cloth.

```
POST /rigidGarmentModel HTTP/1.1
Host: https://novoloom.com/simulations
Connection: close
Accept: */*
Content-Type: application/json
Accept: application/json

{
  "vertices": [
    [0, 0, 0],
    [1, 0, 0],
    [1, 1, 0],
    [0, 1, 0]
  ],
  "indices": [
    [0, 1],
    [1, 2],
    [3, 4],
    [4, 0],
    [1, 3]
  ]
}
    
    

```
