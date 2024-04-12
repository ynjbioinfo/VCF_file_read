import pandas as pd

with open("example.vcf", "r") as f:
    lines = f.readlines()
    chrom_index = [i for i, line in enumerate(lines) if line.strip().startswith("#CHROM",)]
    data = lines[chrom_index[0]:]
    header = data[0].strip().split("\t")
    informations = [d.strip().split("\t") for d in data[1:]]
vcf = pd.DataFrame(informations, columns=header)
columns = ["#CHROM", "ID", "ALT", "REF"]
vcf1 = pd.DataFrame(vcf, columns=columns)
print(vcf1)
