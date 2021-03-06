<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [constructor](#constructor)
-   [findUnsavedLeafNodes](#findunsavedleafnodes)
-   [set](#set)
-   [get](#get)
-   [tree](#tree)
-   [flush](#flush)

## constructor

[index.js:19-26](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L19-L26 "Source code on GitHub")

**Parameters**

-   `dag`  
-   `ipfsDag` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** an instance of [ipfs.dag](https://github.com/ipfs/interface-ipfs-core/tree/master/API/dag#dag-api)

## findUnsavedLeafNodes

[index.js:46-59](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L46-L59 "Source code on GitHub")

given a node on the graph this returns all the leaf node that have not yet been saved

**Parameters**

-   `node` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** 

## set

[index.js:69-95](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L69-L95 "Source code on GitHub")

sets a value on a root object given its path

**Parameters**

-   `node` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
-   `path` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `value` **any** 
-   `noLink` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** if true, value is added as a plain object instead of a link

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 

## get

[index.js:105-109](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L105-L109 "Source code on GitHub")

traverses an object's path and returns the resulting value in a Promise

**Parameters**

-   `node` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
-   `path` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 
-   `dropOptions` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether to add the encoding options of the
    nodes when loading from IPFS. Defaults to true

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 

## tree

[index.js:153-172](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L153-L172 "Source code on GitHub")

Resolves all the links in an object and does so recusivly for N `level`

**Parameters**

-   `node` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
-   `levels` **Integer**  (optional, default `1`)
-   `dropOptions` **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** whether to add the encoding options of the
    nodes when loading from IPFS. Defaults to true

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 

## flush

[index.js:197-210](https://github.com/wulfraem/js-ipld-graph-builder/blob/6e85b3c8962021745a51de272ad6def2477deaac/index.js#L197-L210 "Source code on GitHub")

flush an object to ipfs returning the resulting CID in a promise

**Parameters**

-   `node` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 
-   `opts` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** encoding options for [`dag.put`](https://github.com/ipfs/interface-ipfs-core/tree/master/API/dag#dagput) (optional, default `{}`)
    -   `opts.onHash` **[Function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function)** a callback that happens on each merklized node. It is given two arguments `hash` and `node` which is the node that was hashed

Returns **[Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)** 
