# pinkVocalTransformer
## Abstract
Articulatory synthesis aims to model the vocal tract and simulate articulator motion to generate speech, but traditional approaches face challenges in complexity, data acquisition, and variability. We propose PinkVocalTransformer, a Transformer-based black-box model for acoustic-to-articulatory inversion, leveraging the Pink Trombone synthesizer. A parallel dataset of acoustic signals and articulatory parameters is generated under static configurations to enable supervised learning of articulatory mappings. To improve generalization, we incorporate pretrained speech models for feature extraction.

Unlike prior black-box methods that estimate individual articulator trajectories, our model directly reconstructs the overall vocal tract shape, reducing ambiguity. The regression task is reformulated as classification to enhance training stability, and HuBERT embeddings are used to improve performance on real-world audio. Experimental results demonstrate that PinkVocalTransformer outperforms existing black-box methods in vowel reconstruction tasks, offering a data-driven and efficient approach to articulatory synthesis.
## Audio Samples
### Simple Vowel Samples
#### /a/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/a.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_a.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_a.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_a.wav"></audio></td>
  </tr>
</table>

#### /e/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/e.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_e.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_e.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_e.wav"></audio></td>
  </tr>
</table>

#### /o/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/o.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_o.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_o.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_o.wav"></audio></td>
  </tr>
</table>

#### /u/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/u.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_u.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_u.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_u.wav"></audio></td>
  </tr>
</table>

### Vowel-to-Vowel Samples
#### /eiu/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/eiu.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_eiu.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_eiu.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_eiu.wav"></audio></td>
  </tr>
</table>

#### /aio/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/aio.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_aio.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_aio.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_aio.wav"></audio></td>
  </tr>
</table>

#### /oiu/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/oiu.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_oiu.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_oiu.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_oiu.wav"></audio></td>
  </tr>
</table>

#### /ieaou/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/ieaou.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_ieaou.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_ieaou.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_ieaou.wav"></audio></td>
  </tr>

#### /roy/
<table>
  <tr>
    <th>Original</th>
    <th>PinkVocalTransformer</th>
    <th>VAE+Synth slow</th>
    <th>VAE+Synth fast</th>
  </tr>
  <tr>
    <td><audio controls src="audio/orig/roy.wav"></audio></td>
    <td><audio controls src="audio/best_audio/pt_roy.wav"></audio></td>
    <td><audio controls src="audio/VAE_slow/vae_roy.wav"></audio></td>
    <td><audio controls src="audio/VAE_fast/vae_roy.wav"></audio></td>
  </tr>
</table>
