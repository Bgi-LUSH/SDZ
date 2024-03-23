# SDZ : Lossless FASTQ compression with ultra-high compression rate

### base_compressor

./base_compressor ./base.fq ./out.base.sdz

The first parameter is the input file containing only base, and the second parameter is the output file after compressing base. 




### qual_compressor

./qual_compressor ./base.fq ./qual.fq ./out.qual.sdz
 
The first parameter is the input file containing only base, the second parameter is the input file containing only qual, and the third     parameter is the output file after compressing qual.



### run in docker
docker load -i compress_tool_docker.tar.gz

```bash
## compression for base
docker run -v  /YOUR_PATH/:/contain_PATH  compress_tool:latest  base_compressor /YOUR_PATH/base.sample /YOUR_PATH/out.base.sdz

## compression for quality scores 
docker run -v  /YOUR_PATH/:/contain_PATH  compress_tool:latest  qual_compressor /YOUR_PATH/base.sample /YOUR_PATH/qual.sample /YOUR_PATH/out.qual.sdz 

```  
