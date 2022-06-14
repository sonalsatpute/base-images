# base-images


### create directory for all the projects

```bash
RUN for FILE in `ls *.csproj`; \
    do \
      directory_name=${FILE%.*}; \
#      echo $directory_name; \
      mkdir $directory_name; >/dev/null 2>&1; \
      mv $FILE $directory_name/$FILE; \
    done
```
