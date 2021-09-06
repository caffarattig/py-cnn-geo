# Outdated project!!
The project is now under the [Laboratorio de Sistemas Inteligentes](https://github.com/labsin-uncuyo). Please refer to [this link](https://github.com/labsin-uncuyo/py-cnn-geo) to access the last version.

## py-cnn-geo
CNN architecture for Forest-No Forest mask generation based on SRTM and Landsat-8 information.


## Dataset
Bellow there's a table describing the different files involved in the contruction of each zone of the dataset, the coverage, number of points for each class, and usage of the zone (training or testing).
<table>
  <thead>
    <tr>
      <th>Zone</th>
      <th>Coverage</th>
      <th>SRTM file</th>
      <th>Landsat-8 files</th>
      <th>FNF file</th>
      <th>Usage</th>
      <th>F-NF Points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>
        25º0'0"S - 53º0'0"W to<br>
        26º0'0"S - 52º0'0"W</td>
      <td>s26_w053_1arc_v3</td>
      <td>
        LC08_L1TP_223077_20140204_20170426_01_T1<br>
        LC08_L1TP_223078_20140204_20170426_01_T1<br>
        LC08_L1TP_222077_20140301_20170425_01_T1<br>
        LC08_L1TP_222078_20140301_20170425_01_T1
      </td>
      <td>S25W053_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 10363584<br>
        F: 2596416
      </td>
    </tr>
    <tr>
      <td>2</td>
      <td>
        25º0'0"S - 52º0'0"W to<br>
        26º0'0"S - 51º0'0"W</td>
      <td>s26_w052_1arc_v3</td>
      <td>
        LC08_L1TP_222077_20140301_20170425_01_T1<br>
        LC08_L1TP_222078_20140301_20170425_01_T1
      </td>
      <td>S25W052_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 5739929<br>
        F: 7220071
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td>
        25º0'0"S - 51º0'0"W to<br>
        26º0'0"S - 50º0'0"W</td>
      <td>s26_w051_1arc_v3</td>
      <td>
        LC08_L1TP_221077_20140206_20170426_01_T1<br>
        LC08_L1TP_221078_20140206_20170426_01_T1
      </td>
      <td>S25W051_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 7125519<br>
        F: 5834481
      </td>
    </tr>
    <tr>
      <td>4</td>
      <td>
        25º0'0"S - 50º0'0"W to<br>
        26º0'0"S - 49º0'0"W</td>
      <td>s26_w050_1arc_v3</td>
      <td>
        LC08_L1TP_221077_20140206_20170426_01_T1<br>
        LC08_L1TP_221078_20140206_20170426_01_T1<br>
        LC08_L1TP_220077_20140130_20170426_01_T1<br>
        LC08_L1TP_220078_20140130_20170426_01_T1
      </td>
      <td>S25W050_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 5202917<br>
        F: 7757083
      </td>
    </tr>
    <tr>
      <td>5</td>
      <td>
        26º0'0"S - 53º0'0"W to<br>
        27º0'0"S - 52º0'0"W</td>
      <td>s27_w053_1arc_v3</td>
      <td>
        LC08_L1TP_223078_20140204_20170426_01_T1<br>
        LC08_L1TP_222078_20140301_20170425_01_T1<br>
        LC08_L1TP_222079_20140301_20170425_01_T1
      </td>
      <td>S26W053_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 10081411<br>
        F: 2878589
      </td>
    </tr>
    <tr>
      <td>6</td>
      <td>
        26º0'0"S - 52º0'0"W to<br>
        27º0'0"S - 51º0'0"W</td>
      <td>s27_w052_1arc_v3</td>
      <td>
        LC08_L1TP_222078_20140301_20170425_01_T1<br>
        LC08_L1TP_222079_20140301_20170425_01_T1<br>
        LC08_L1TP_221078_20140206_20170426_01_T1<br>
        LC08_L1TP_221079_20140206_20170426_01_T1
      </td>
      <td>S26W052_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 3763615<br>
        F: 9196385
      </td>
    </tr>
    <tr>
      <td>7</td>
      <td>
        26º0'0"S - 51º0'0"W to<br>
        27º0'0"S - 50º0'0"W</td>
      <td>s27_w051_1arc_v3</td>
      <td>
        LC08_L1TP_221078_20140206_20170426_01_T1<br>
        LC08_L1TP_221079_20140206_20170426_01_T1
      </td>
      <td>S26W051_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 4077598<br>
        F: 8882402
      </td>
    </tr>
    <tr>
      <td>8</td>
      <td>
        26º0'0"S - 50º0'0"W to<br>
        27º0'0"S - 49º0'0"W</td>
      <td>s27_w050_1arc_v3</td>
      <td>
        LC08_L1TP_221078_20140206_20170426_01_T1<br>
        LC08_L1TP_221079_20140206_20170426_01_T1<br>
        LC08_L1TP_220078_20140130_20170426_01_T1<br>
        LC08_L1TP_220079_20140130_20170426_01_T1
      </td>
      <td>S26W050_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 2860139<br>
        F: 10099861
      </td>
    </tr>
    <tr>
      <td>9</td>
      <td>
        27º0'0"S - 53º0'0"W to<br>
        28º0'0"S - 52º0'0"W</td>
      <td>s28_w053_1arc_v3</td>
      <td>
        LC08_L1TP_222079_20140301_20170425_01_T1
      </td>
      <td>S27W053_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 9604649<br>
        F: 3355351
      </td>
    </tr>
    <tr>
      <td>10</td>
      <td>
        27º0'0"S - 52º0'0"W to<br>
        28º0'0"S - 51º0'0"W</td>
      <td>s28_w052_1arc_v3</td>
      <td>
        LC08_L1TP_222079_20140301_20170425_01_T1<br>
        LC08_L1TP_221079_20140206_20170426_01_T1
      </td>
      <td>S27W052_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 8132216<br>
        F: 4827784
      </td>
    </tr>
    <tr>
      <td>11</td>
      <td>
        27º0'0"S - 51º0'0"W to<br>
        28º0'0"S - 50º0'0"W</td>
      <td>s28_w051_1arc_v3</td>
      <td>
        LC08_L1TP_221079_20140206_20170426_01_T1
      </td>
      <td>S27W051_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 5461194<br>
        F: 7498806
      </td>
    </tr>
    <tr>
      <td>12</td>
      <td>
        27º0'0"S - 50º0'0"W to<br>
        28º0'0"S - 49º0'0"W</td>
      <td>s28_w050_1arc_v3</td>
      <td>
        LC08_L1TP_221079_20140206_20170426_01_T1<br>
        LC08_L1TP_220079_20140130_20170426_01_T1
      </td>
      <td>S27W050_15_FNF_F02DAR</td>
      <td>Training</td>
      <td>
        NF: 3720423<br>
        F: 9239577
      </td>
    </tr>
    <tr>
      <td>13</td>
      <td>
        28º0'0"S - 51º0'0"W to<br>
        29º0'0"S - 50º0'0"W</td>
      <td>s29_w051_1arc_v3</td>
      <td>
        LC08_L1TP_221080_20140206_20170426_01_T1<br>
        LC08_L1TP_221079_20140206_20170426_01_T1<br>
        LC08_L1TP_220080_20140130_20170426_01_T1
      </td>
      <td>S28W051_15_FNF_F02DAR</td>
      <td>Testing</td>
      <td>
        NF: 7776871<br>
        F: 5183129
      </td>
    </tr>
  </tbody>
</table>
