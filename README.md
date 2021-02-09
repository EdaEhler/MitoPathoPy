# MitoPathoPy
Search for potential pathological mutations in your human full mtDNA sequence  
Author: Edvard Ehler, PhD (edvard.ehler@img.cas.cz)  
Year: 2020  

---------------------------
This tool will search for the (potential) pathological mutations in you mtDNA samples. To get the right input format, please, use the Haplogrep 2 (https://haplogrep.i-med.ac.at/app/index.html) tool to turn your sequences (fastas) into HSD format file. Haplogrep can be also downloaded and run localy (https://github.com/seppinho/haplogrep-cmd). Pathological mtDNA mutations are taken from data published at https://www.mitomap.org/MITOMAP.

HSD format is a simple, tab delimited text file with 4 or more columns. Here are the examples taken from Haplogrep GitHub and their online test data:

    
    ID	 Range	 Haplogroup	 Polymorphisms
    Sample1	1-16569	?	263G	315.1C	750G	1041G	1438G	4769G	8860G	9410G	12358G	13656C	15326G	16189C	16192T	16519C
    Sample2 1-16569 H100 263G 315.1C 750G 1041G 1438G 4769G 8860G 9410G 12358G 13656C 15326G 16189C 16192T 16519C
    Sample3 1-16569 ? 73G 263G 315.1C 750G 1438G 3010A 3107C 4769G 5111T 8860G 10257T 12358G 15326G 16145A 16222T 16519C
    Sample4	16024-16569;1-576;2092;3552;4071;4491;4833;4883;8414;8473;9090;9824;10397;10400;11959;11969;12372;12771;13563;14502;14569;15487;	G2a1d	73G	260A	263G	309.1C	315.1C	489C	4833G	10400T	13563G	14569A	16183C	16189C	16193.1C	16223T	16278T	16362C
    Sample5	16024-16569;1-576;1119;1719;1736;3547;3970;4820;5417;8277;8281-8289;8392;9123;10310;10398;11914;12007;12338;12358;12705;12714;14502;15535;	B4h	73G	263G	309.1CC	315.1C	523d	524d	8281d	8282d	8283d	8284d	8285d	8286d	8287d	8288d	8289d	16129A	16182C	16183C	16189C	16217C	16261T	16319A	16497G 
    

### Workflow
1. Prepare your samples into HSD format.
2. With `mitopatho.py` and `mitopatho_db_v1.pickle` in you directory run: `mitopatho.py -i your_input.hsd -o output.txt`
3. The output file is tab separated file, one line per sample, following format:

        sample_name   allele1,disease1,status1;allele2,disease2,status2;allele3,disease3,status3;...


We invite you to check our **Ancient mtDNA Database** at: https://amtdb.org/

If you use this tool in you research, please, consider citing our article:
Ehler E, Novotný J, Juras A, Chyleński M, Moravčík O, Pačes J. AmtDB: a database of ancient human mitochondrial genomes. Nucleic acids research. 2019 Jan 8;47(D1):D29-32. https://academic.oup.com/nar/article-abstract/47/D1/D29/5106144
