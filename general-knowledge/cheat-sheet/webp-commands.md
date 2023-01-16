# WebP  

## APT Package Manager Installation  
```bash
sudo apt install webp
```

## Other Package Managers 
```bash
wget -c https://storage.googleapis.com/downloads.webmproject.org/releases/webp/libwebp-0.6.1-linux-x86-32.tar.gz
```

## Export webp path
```
export PATH=$PATH:~/libwebp-0.6.1-linux-x86-32/bin
```

## cwebp   
Options:
 `-q` <- defines the output quality of the image from 0 to 100 
 `-o` <- specifies the output file
 
### Single file
```bash
cwebp -q 60 Cute-Baby-Girl.png -o Cute-Baby-Girl.webp
```

```bash
bash./cwebp -q 60 Cute-Baby-Girl.png -o Cute-Baby-Girl.webp
```

### Batch Processing 
```bash
for file in *.png ; 
do cwebp -q 50 "$file" -o "${file%.png}.webp"; 
done
```

## vwebp

