# Supplmentary Figure 7
```{r}
# Load libraries
library(ggtree)
library(ape)
library(phytools)

# Load LINcode data
lincodes <- read.csv("FINAL_DATA/short_LINcodes_cgST.csv", header=TRUE) %>% na.omit()

# Add lineage LIN code as a single string
lincodes$gy <- paste(lincodes$L1,lincodes$L2,lincodes$L3, sep = "_")

# Import phylogeny
tree3 <- midpoint.root(read.newick("19k_tree.nwk"))

# Plot tree, coloring tippoints by the most prevalent lineages
ggtree(tree3, layout="circular", size=0.1, color="grey30") %<+% 
  subset(lincodes, gy=="0_58_0" | gy=="0_15_4" | gy=="0_15_0" | gy=="0_0_0" | gy=="0_75_0" | gy=="0_20_1" | 
           gy=="0_11_3" | gy=="0_55_1" | gy=="0_11_8" | gy=="0_55_1" | gy=="0_75_0" | gy=="0_57_0" | 
           gy=="0_145_2" | gy=="0_130_1" | gy=="0_10_0" | gy=="0_169_0" | gy=="0_232_1" | gy=="0_74_0" | gy=="0_21_0" | gy=="0_237_0" | gy=="0_265_0" | gy=="0_310_0" ) +  
  theme(legend.position = "none") + 
  geom_tippoint(aes(color=gy), na.rm = TRUE) +
 # scale_color_manual(values = "#D89000", na.value = NA) +
  geom_cladelabel(node=2518, color='black', label = "0_58_0", offset = 0.00015, barsize = 0.45, hjust = 1.5) +
geom_cladelabel(node=2927, color='black', label = "0_15_4", offset = 0.00015, barsize = 0.45,hjust = 1.5)  +
geom_cladelabel(node=2871, color='black', label = "0_15_0", offset = 0.00015, barsize = 0.45,hjust = 1.5) +
geom_cladelabel(node=2647, color='black', label = "0_0_0", offset = 0.00015, barsize = 0.45,hjust = 1.5) + 
geom_cladelabel(node=2193, color='black', label = "0_75_0", offset = 0.00015, barsize = 0.45,hjust = 1.5) +
geom_cladelabel(node=3439, color='black', label = "0_20_1", offset = 0.00015, barsize = 0.45,hjust = 1) +
geom_cladelabel(node=1968, color='black', label = '0_11_3', offset = 0.00015, barsize = 0.45,hjust = 1.5) + 
geom_cladelabel(node=2496, color='black', label = '0_55_1', offset = 0.00015, barsize = 0.45,hjust = 1.5) +
geom_cladelabel(node=2029, color='black', label = '0_11_8', offset = 0.00015, barsize = 0.45,hjust = 1.5)  +
geom_cladelabel(node=2193, color='black', label = "0_75_0", offset = 0.00015, barsize = 0.45,hjust = 1.5) +
geom_cladelabel(node=2783, color='black', label = "0_57_0", offset = 0.00015, barsize = 0.45,hjust = 1.5)  +
geom_cladelabel(node=3752, color='black', label = "0_145_2", offset = 0.00015, barsize = 0.45, hjust=-1) +
geom_cladelabel(node=3077, color='black', label = "0_130_1", offset = 0.00015, barsize = 0.45) + 
geom_cladelabel(node=3019, color='black', label = "0_10_0", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=3619, color='black', label = "0_169_0", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=2430, color='black', label = "0_232_1", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=2147, color='black', label = "0_74_0", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=2386, color='black', label = "0_237_0", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=3524, color='black', label = "0_21_0", offset = 0.00015, barsize = 0.45) +
geom_cladelabel(node=3201, color='black', label = "0_265_0", offset = 0.00015, barsize = 0.45, hjust=1) +
geom_cladelabel(node=3259, color='black', label = "0_310_0", offset = 0.00015, barsize = 0.45, hjust=1)
```
