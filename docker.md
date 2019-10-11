# Docker

## &lt;none&gt;/&lt;none&gt; on docker images

These are dangling images as opposed to the intermediate ones seen via `docker images -a`. They can be safely pruned with:

`docker rmi (docker images -f "dangling=true" -q) --force` 

as they are not used \(not in any way in a child/parent relationship as in the `-a` counterpart\) and are only taking disk space. Explanation can be found e.g. [here](http://www.projectatomic.io/blog/2015/07/what-are-docker-none-none-images/). 

`docker build` has an `--rm` option, which "Removes intermediate containers after a successful build". Apparently it removes the images connected with them as well, because I'm not seeing any more `<none>` ones.

