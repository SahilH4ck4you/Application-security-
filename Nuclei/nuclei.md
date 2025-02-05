### JS Files:-
```nuclei -l js_for_nuclei.txt -t javascript,file/js,file/keys,miscon,expos,a=take,panel```


### Web:-
```nuclei -l subs.txt -t file/js,file/keys,file/logs,file/audit,miscon,expos,a=take,panel```


### Android:-

- Decompile/Unzip App
- Open Terminal in the App's Path
- Run the command:- ```find . | tee for_nuclei.txt```
- Now run Nuclei:- ```nuclei -l for_nuclei.txt -t file/android,file/keys,miscon,expos,panel```
