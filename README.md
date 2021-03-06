# Ahmed Bluff Body CFD Validation
The purpose of this repo is to serve as a starting point for further automotive/motorsport CFD or as a resource for CFD code validation. The Ahmed bluff body geometry is included so anyone can use it in their simulations. If you would like to add a validation case, please open a pull request and I'll add it! Thanks!
<center><p><img src="docs/ahmed.gif"></p></center>

### Current results

| case_id | case directory | decklid angle | solver | turbulence model | c<sub>d</sub> | c<sub>d</sub> error | c<sub>l</sub> | c<sub>l</sub> error |
| --- | :--- | --- | --- | --- | --- | --- | --- | --- |
| 1-A | openfoam_rans | 25 | simpleFoam | RAS - kOmegaSST | 0.299 | 0.000 | 0.339 | -0.006 |
| 1-B | openfoam_rans | 35 | simpleFoam | RAS - kOmegaSST | | | | |
| 2-A | openfoam_les | 25 | pisoFoam | LES - SpalartAllmarasDDES | | | | | 
| 2-B | openfoam_les | 35 | pisoFoam | LES - SpalartAllmarasDDES | | | | |
* c_d and c_l values are calculated by averaging the last 50 time steps for rans case

<b>Mesh properties by case </b>
| case_id | cell count | y+ min | y+ max | y+ mean |  snappyHexMeshDict |
| --- | --- | --- | --- | --- | --- |
| 1-A | 8,250,693 | 0.313 | 340.130 | 13.244 | snappyHexMeshDict_1A |
| 1-B | | | | | snappyHexMeshDict_1B |
| 2-A | | | | | snappyHexMeshDict_2A |
| 2-B | | | | | snappyHexMeshDict_2B |
* y+ values are for ahmed-body only


### Existing results
<table style="width:100%">
  <tr>
    <td>type</td>
    <td>decklid angle</td>
    <td>c<sub>d</sub></td>
    <td>c<sub>l</sub></td>
    <td>solver</td>
    <td>source</td>
  </tr>
  <tr>
    <td>exp</td>
    <th rowspan="7">25</th>
    <td>0.299</td>
    <td>0.345</td>
    <td>---</td>
    <th rowspan="11"><a href="https://online.tugraz.at/tug_online/voe_main2.getVollText?pDocumentNr=81599">link</a></th>
  </tr>
  <tr>
    <th rowspan="6">cfd</th>
    <td>0.300</td>
    <td>0.316</td>
    <th rowspan="6">simpleFoam</th>
  </tr>
  <tr>
    <td>0.266</td>
    <td>0.325</td>
  </tr>
  <tr>
    <td>0.274</td>
    <td>0.330</td>
  </tr>
  <tr>
    <td>0.250</td>
    <td>0.306</td>
  </tr>
  <tr>
    <td>0.260</td>
    <td>0.305</td>
  </tr>
  <tr>
    <td>0.301</td>
    <td>0.307</td>
  </tr>
  <tr>
    <td>exp</td>
    <th rowspan="4">35</td>
    <td>0.279</td>
    <td>0.004</td>
    <td>---</td>
  <tr>
    <th rowspan="3">cfd</th>
    <td>0.313</td>
    <td>0.212</td>
    <th rowspan="3">simpleFoam</th>
  </tr>
  <tr>
    <td>0.292</td>
    <td>0.156</td>
  </tr>
  <tr>
    <td>0.247</td>
    <td>0.159</td>
  </tr>
  <tr>
    <th rowspan="4">cfd</th>
    <td align="center">20</td>
    <td>0.262</td>
    <td>0.284</td>
    <th rowspan="4">Ansys Fluent</th>
    <th rowspan="4"><a href="http://www.iosrjournals.org/iosr-jmce/papers/vol12-issue4/Version-3/M012438794.pdf">link</a></th>
  </tr>
  <tr>
    <td align="center">30</td>
    <td>0.298</td>
    <td>0.348</td>
  </tr>
  <tr>
    <td align="center">35</td>
    <td>0.295</td>
    <td>0.206</td>
  </tr>
  <tr>
    <td align="center">40</td>
    <td>0.250</td>
    <td>0.008</td>
  </tr>
</table>
