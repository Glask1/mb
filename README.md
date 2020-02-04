# mb
Shell script to generate music blog pages for https://glask.info/music
```
root of site
│   index.html   
└───artists folder
    BASE HTMLS:
    │   artist_frame.html
    │   artist_insert.html
    │   rank_frame.html
    │   rank_insert.html
    │   insert.html
    │   artist.html
    │   mb
    GENERATED:
    │   index.html
    │   rank.html
    │   list
    │   artist_1.html
    │   artist_2.html
    │   ...
```

## commands
    ./mb n
    
add a new album to the review catalog. 
- Creates artist_name.html (if needed) from artist.html, and adds insert.html for the album. 
- Fills in information based on what is inputted by user. 
- Then adds album to list, calls other two functions.
- adds album to ../index.html after the flag <!---new--->
![new](https://glask.info/blog/img/mb_example.png)
```
    ./mb i
```
update autogenerated index of all artists. 
- Takes in artist_frame.html, inserts an artist_insert.html for each artist in list.
```
    ./mb r
```
update autocalculated ranking list. 
- Takes in rank_frame.html, inserts a rank_frame.html for top albums in list, sorted.
