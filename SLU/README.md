# Spoken Language Understanding (SLU)

The SLU Benchmark used for the **LeBenchmark** is **MEDIA** (**link toward the data coming soon**).

The system used is based on Sequence-to-Sequence models and is coded for the [Fairseq library](https://github.com/pytorch/fairseq) (**code coming soon**).
The encoder is similar to the pyramidal LSTM-based encoder proposed in the [Listen, attend and spell paper](https://arxiv.org/abs/1508.01211), the only difference is that we compute the mean of two consecutive hidden states for reducing the output size between two layers, instead of concatenating them like in the original model.
The decoder is similar to the one used in our previous work published at [ICASSP 2020](http://www.marcodinarelli.it/publications/2020_ICASSP_EndToEndSLU.pdf). The differences in this case are that we use two attention mechanisms, one for attending the encoder hidden states, and the other for attending all the previous predictions, instead of using only the previous one like in the original decoder.

<table>
  <thead>
    <tr>
      <th colspan="4"> Token decoding (Word Error Rate)</th>
    </tr>  
    <tr>
      <th> Model </th>
      <th> Input Features </th>
      <th> DEV ER </th>
      <th> TEST ER </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td> Kheops+Basic </td> <td> Spectrogram </td> <td> 36.25 </td> <td> 37.16 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2 En base </td> <td> 19.80 </td> <td> 21.78 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2 En large </td> <td> 24.44 </td> <td> 26.96 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2-S Fr base </td> <td> 23.11 </td> <td> 25.22 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2-S Fr large </td> <td> 18.48 </td> <td> 19.92 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2-M Fr base </td> <td> 14.97 </td> <td> 16.37 </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> W2V2-M Fr large </td> <td> <b>11.77</b> </td> <td> <b>12.85</b> </td>
    </tr>
    <tr>
      <td> Kheops+Basic </td> <td> XLSR53 large </td> <td> 14.98 </td> <td> 15.74 </td>
    </tr>
  </tbody>
  
  <thead>
    <tr>
      <th colspan="4"> Concept decoding (Concept Error Rate)</th>
    </tr>  
    <tr>
      <th> Model </th>
      <th> Input Features </th>
      <th> DEV ER </th>
      <th> TEST ER </th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td> Kheops+Basic </td> <td> Spectrogram </td> <td> xx.xx </td> <td> xx.xx </td>
    </tr>
  </tbody>
  
 </table>