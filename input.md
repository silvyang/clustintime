# Input
The inputs are the parameters or arguments that you can pass to the function.

## Configuration Options and Parameters:
- data_paths (str or path, required): A list of paths to the data files that the function will use for clustering.
- mask_path (str or path, required): The path to a mask file, which likely represents a region of interest in the data.
- component (str, optional, default="whole"): Specifies which component of the data to use for clustering. It might refer to specific features or channels in the data. The options are `whole`, `positive`, `negative`.
- timings_file (str or path, optional): Path to a file containing timing information.
- correlation (str, optional, default="standard"): The type of correlation to use for clustering. It could be Pearson, Spearman, etc. The options are `standard`, `window`.
- process_type (str, optional, default="None"): The type of data processing to be applied. The options are `None`, `double`, `thr`, `RSS`, `window`
- window_size (int, optional, default=1): The size of the window for processing data.
- near (int, optional, default=1): Parameter related to the clustering algorithm.
- thr (int, optional, default=95): Threshold value for clustering.
- contrast (float, optional, default=1):  Range of values for the correlation matrixes.
- repetition_time (float, optional, default=0.5): The repetition time for the data.
- affinity (optional, default="euclidean"): The affinity metric for the clustering algorithm.
- linkage (optional, default="ward"): The linkage method for hierarchical clustering.
- algorithm (str, optional, default="infomap"): The clustering algorithm to use (e.g., "infomap"). The options are `infomap`, `Agglomerative`, `Louvain`, `Greedy` and `KMeans`.
- consensus (bool, optional, default=False): Boolean that indicates whether to use consensus clustering in the algorithm or not.
- n_clusters (int, optional, default=7): Desired number of groups for the K Means algorithm.
- save_maps (bool, optional, default=True): Boolean that indicates whether the results must be saved or not.
- aving_dir (str or path, optional, default="."): The directory where the results will be saved.
- prefix (str, optional): A prefix to be added to the saved files.
- seed (optional, default=0): Seed for random number generation.
- generate_dyneusr_graph (bool, optional, default=False): Whether to generate a graph using DyNeUsR.
- title (str, optional): Title for the plot or output.

## How to Use
Example usage:
`````
clustintime(
    data_paths="path/to/fmri_data.nii.gz",
    mask_path="path/to/mask.nii.gz",
    component="whole",
    timings_file=None,
    correlation="standard",
    process_type=None,
    window_size=1,
    near=1,
    thr=95,
    contrast=1,
    repetition_time=0.5,
    affinity="euclidean",
    linkage="ward",
    algorithm="infomap",
    consensus=False,
    n_clusters=7,
    save_maps=True,
    saving_dir="output/",
    prefix="result",
    seed=0,
    generate_dyneusr_graph=False,
    title="Clustintime Analysis",
)
`````
