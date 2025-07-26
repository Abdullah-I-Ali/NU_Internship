# 📊 Comprehensive Comparison of Toehold Switch Design Tools

<table>
<thead>
<tr>
<th>Tool</th>
<th>Thermodynamics &amp; Structure</th>
<th>Design Capabilities</th>
<th>Performance Prediction</th>
<th>I/O &amp; Interoperability</th>
<th>Performance &amp; Usability</th>
<th>Software Quality</th>
<th>Experimental Integration</th>
<th>Advanced Features</th>
</tr>
</thead>
<tbody>
<tr><td><strong>NUPACK</strong></td>
<td>Turner’06, ensemble defect, partition function, no pseudoknots, multi‑strand folding</td>
<td>Inverse folding, GC constraints, FASTA input</td>
<td><span style="color:red">No ON/OFF predictor</span>, ΔG-only</td>
<td>CLI/Python API, FASTA in, CT/dot-bracket out</td>
<td>Fast C++, multithreaded</td>
<td>BSD license; extensive docs; ~1000 citations</td>
<td>Widely used; synthesis‑ready sequences</td>
<td>Multi-strand modeling; constraint-based</td>
</tr>

<tr><td><strong>ViennaRNA</strong></td>
<td>Turner’04 model; base-pair probabilities; suboptimal folding; no pseudoknots</td>
<td>RNAinverse, constraints, cofolding</td>
<td><span style="color:red">No ON/OFF predictor</span></td>
<td>CLI/GUI/Python; FASTA input; dot‑bracket/PS output</td>
<td>Very fast C implementation</td>
<td>GPL3; ~2000 citations; actively maintained</td>
<td>Broad folding validation</td>
<td>RNA–RNA interaction; kinetic tools (Kinfold)</td>
</tr>

<tr><td><strong>RNAstructure</strong></td>
<td>Turner’04; partition-function; pseudoknots via ProbKnot</td>
<td>Limited inverse design; CT/FASTA input</td>
<td><span style="color:red">No ON/OFF predictor</span></td>
<td>GUI/CLI; FASTA/CT input; dot‑bracket/CT output</td>
<td>C++, moderate speed, GUI support</td>
<td>Free academic; moderate docs</td>
<td>Dynalign for RNA interactions</td>
<td>Pseudoknot prediction; suboptimal sampling</td>
</tr>

<tr><td><strong>Mfold/UNAFold</strong></td>
<td>Zuker/Turner’99; melting Tm; no pseudoknots</td>
<td>Structure prediction only</td>
<td><span style="color:red">No prediction</span></td>
<td>Web/CLI; FASTA in; CT/HTML out</td>
<td>Older, slower code</td>
<td>Legacy support; minimal updates</td>
<td>Used for visualization</td>
<td>Basic folding only</td>
</tr>

<tr><td><strong>Toeholder</strong></td>
<td>NUPACK-based MFE; no pseudoknots</td>
<td>Batch design, BLAST off-target check</td>
<td>ΔΔG ranking; <span style="color:red">no ON/OFF predictor</span></td>
<td>CLI, FASTA input, CSV out, BLAST</td>
<td>Moderate speed; depends on NUPACK</td>
<td>GPL license; GitHub docs</td>
<td>Used in iGEM; limited wet‑lab validation</td>
<td>Trigger specificity filtering</td>
</tr>

<tr><td><strong>Toehold Creator</strong></td>
<td>ViennaRNA MFE; no pseudoknots</td>
<td>Switch + RPA primer design</td>
<td><span style="color:red">No ON/OFF predictor</span></td>
<td>CLI; FASTA + primer params; CSV out</td>
<td>Moderate speed</td>
<td>GPL‑3.0; limited citations</td>
<td>iGEM tool; no published wet‑lab data</td>
<td>Integrated RBS/primer design</td>
</tr>

<tr><td><strong>CUHK Web Tool</strong></td>
<td>NUPACK backend; no pseudoknots</td>
<td>Web-based automated design</td>
<td><span style="color:green">Linear ML score (trained on ~180 switches)</span></td>
<td>Browser input/output; CSV export</td>
<td>Moderate server-side</td>
<td>Academic tool; limited docs</td>
<td>Benchmarked experimentally on ~180 switches</td>
<td>Empirical efficacy scoring</td>
</tr>

<tr><td><strong>DeepToehold</strong> (SASTRA iGEM’19)</td>
<td>ViennaRNA features (structure + ΔG); no pseudoknots</td>
<td>Regex parsing + ViennaRNA; trained regression</td>
<td><span style="color:green">NN predicts dynamic range (R² ≈ 0.5)</span></td>
<td>CLI pipeline; FASTA input</td>
<td>Python-based; modest speed</td>
<td>GPLv3; GitHub; trained on ~230 literature switches</td>
<td>Derived from validated switches</td>
<td>Sequence + energy ML model</td>
</tr>

<tr><td><strong>STORM</strong> (MIT/Wyss)</td>
<td>Extracts ViennaRNA sequence/structure embedding</td>
<td>Trigger/switch redesign suggestions</td>
<td><span style="color:green">CNN predicts ON/OFF; supports redesign</span></td>
<td>Web interface; FASTA input/output</td>
<td>User-friendly server</td>
<td>Published Nature Comm (2020) model SWORD improved STORM R² to 0.75 for ON state by GAN integration over CNN :contentReference[oaicite:1]{index=1}</td>
<td>Experimental data used for redesign validation :contentReference[oaicite:2]{index=2}</td>
<td>CNN-based design optimization, GAN in SWORD</td>
</tr>

<tr><td><strong>ToeholdTools</strong> (City of London iGEM’21)</td>
<td>Uses ViennaRNA/NUPACK structures</td>
<td>Desktop GUI + Python API; offline specificity checks (miRBase)</td>
<td><span style="color:orange">No ON/OFF predictor</span></td>
<td>Offline GUI, Python API, Pandas, FASTA support :contentReference[oaicite:3]{index=3}</td>
<td>Moderate speed; user-friendly</td>
<td>GPLv3; documented; offline package :contentReference[oaicite:4]{index=4}</td>
<td>Designed for miRNA specificity analysis</td>
<td>miRNA specificity, progress tracking, Pandas integration</td>
</tr>

<tr><td><strong>SwitchMi Designer</strong> (UParis BME iGEM’21)</td>
<td>Modified Toeholder/ViennaRNA; tailor-made for miRNA length (7+ bases) :contentReference[oaicite:5]{index=5}</td>
<td>Library generation for miRNA triggers; adapted secondary domain structure</td>
<td><span style="color:red">No ON/OFF predictor</span></td>
<td>CLI, FASTA of miRNA triggers</td>
<td>MIT‑licensed; Python-based</td>
<td>Open-source; designed for miRNA detection</td>
<td>Designed explicitly for miRNA triggers (18–25 nt)</td>
<td>Customized trigger-length design with uni‑paired base constraints</td>
</tr>

<tr><td><strong>Genoswitch</strong> (City of London UK’23)</td>
<td>Uses NUPACK + multi-miRNA trigger modeling</td>
<td>Multi-miRNA AND gate design; UI + appimage; miRBase integration :contentReference[oaicite:6]{index=6}</td>
<td><span style="color:green">Predicted efficacy via MFE and exposure metrics</span></td>
<td>Appimage GUI; miRBase import; FASTA I/O</td>
<td>Desktop UI; offline app; NUPACK backend</td>
<td>Open-source; shipped via appimage; updated 2023</td>
<td>Designed for multi-miRNA specificity in diagnostic contexts</td>
<td>AND-gate for >1 miRNA; base exposure analysis; trigger order evaluation</td>
</tr>
</tbody>
</table>
