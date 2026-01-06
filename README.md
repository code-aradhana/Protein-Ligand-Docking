# Protein-Ligand Docking: Exploring Interactions and Predicting Binding Energies

## 📋 Project Overview  
This project performs **protein-ligand docking** simulations using **AutoDock 4.2** to explore the binding interactions between **SARS-CoV-2 Main Protease (Mpro)** and three distinct ligands:  
- **Nirmatrelvir** (Paxlovid component)  
- **Boceprevir** (repurposed HCV drug)  
- **Baicalein** (natural flavonoid)  

The study aims to predict binding poses, calculate binding energies, and compare interaction patterns to evaluate docking’s utility in antiviral drug discovery.

---

## 🎯 Objectives  
1. Perform molecular docking simulations using **AutoDock 4.2**.  
2. Analyze and visualize binding poses and interaction patterns.  
3. Compare predicted binding affinities among the three ligands.  
4. Validate docking results against experimental crystallographic data.  
5. Demonstrate a reproducible computational workflow for structure-based drug discovery.

---

## 🧬 Methodology  
### 1. **Data Collection**  
- **Protein:** SARS-CoV-2 Mpro (PDB ID: `7BQY`) downloaded from the RCSB Protein Data Bank.  
- **Ligands:** Structures retrieved from PubChem and converted from `.sdf` to `.pdb` using Open Babel.  

### 2. **Protein Preparation**  
- Removed water molecules and non-essential heteroatoms using **PyMOL**.  
- Added polar hydrogens and assigned **Kollman charges** in **AutoDock Tools (ADT)**.  
- Saved the final protein structure in `.pdbqt` format.  

### 3. **Ligand Preparation**  
- Optimized ligand geometry and assigned rotatable bonds in ADT.  
- Converted ligands to `.pdbqt` format for docking.  

### 4. **Grid Generation**  
- Defined a grid box around the active site of Mpro for docking simulation.  

### 5. **Docking Simulation**  
- Used the **Lamarckian Genetic Algorithm (LGA)** in AutoDock 4.2.  
- Executed docking via command line using `autogrid4` and `autodock4`.  

### 6. **Results Analysis**  
- Analyzed binding energies, cluster rankings, and RMSD values.  
- Visualized hydrogen bonds and hydrophobic interactions in ADT and PyMOL.  

---

## 📊 Key Results  
| Ligand          | Best Binding Energy (kcal/mol) | Inhibition Constant (Ki) | RMSD (Å) |
|------------------|--------------------------------|--------------------------|----------|
| Nirmatrelvir     | -5.33                          | 123.15 µM                | 5.55     |
| Boceprevir       | -4.81                          | 296.41 µM                | 19.13    |
| Baicalein        | -5.86                          | 50.26 µM                 | 21.86    |

- **Boceprevir** showed the lowest binding energy (-8.2 kcal/mol in crystallographic validation).  
- All ligands formed key hydrogen bonds with catalytic residue **His41**.  
- Docking poses were consistent with experimental data (RMSD ~1.2Å for Boceprevir).  

---

## 🛠️ Tools & Software  
- **AutoDock 4.2** – Docking simulations  
- **AutoDock Tools (ADT)** – Preparation and analysis  
- **PyMOL** – Visualization and structure editing  
- **Open Babel** – File format conversion  
- **RCSB PDB** – Protein structure data  
- **PubChem** – Ligand structure data  

---


## 👩‍🔬 Author  
**Aradhana Kumari**  
Semester 2, Bioinformatics  
[GitHub](https://github.com/code-aradhana)  

---

## 🤝 Acknowledgments  
- **RCSB PDB** and **PubChem** for structural data.  
- **The Scripps Research Institute** for AutoDock tools.  
- **Open-source bioinformatics community** for tutorials and support.

---
