## Ottawa-311 conversion script 

Will show reproducible research setup. (using Docker)

Try running one of these

* http://dockerfile.github.io/#/nodejs
* http://dockerfile.github.io/#/nodejs-runtime

## Online
Go to [SheetJS](http://sheetjs.com/sexql/)

    SELECT ward,call_type,count(*) as count FROM `julSR2014` group by ward,call_type order by count desc

### by hand...

    for i in xlsx/*xlsx; do echo $i; ./node_modules/.bin/xlsx -l $i; done

    for i in xlsx/*xlsx; do echo $i; ./node_modules/.bin/xlsx $i >> csv/`basename $i .xlsx`.csv; done

# docker...

    docker run -it --rm dockerfile/nodejs
    docker run -it --rm dockerfile/nodejs node
    docker run -it --rm dockerfile/nodejs npn

    npm install xlsx --save