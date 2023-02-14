## `grep` Commmand Line Options
source link: [Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/)
* `-i`: this option is to search for a string case insensitively. For example the following input will search for the string **"brown"** in the file , and it will search for words like "Brown", "BROWN", "BRoWn", and etc. (the current directory is ./written_2/non-fiction/OUP/Abernathy)
* input: `$ grep -i "brown" ch2.txt`
* output: the command should return all the lines that contains the string **"brown"** case insensitively.
```
Slater was interested in the financial rewards to be had in the new world while still in England. Mindful of British prohibitions, he committed to memory the design and construction of the spinning mill where he worked. Arriving in New 
York in late 1789, he was referred to Moses Brown in Providence, a prominent merchant who had established a company, Almy and Brown, to develop “frame or water spinning.” Brown responded on December 10, 1789, to Slater’s initial inquiry, saying Almy and Brown certainly wanted the assistance of a person with Slater’s skills because an experimental mill had failed, “no persons being acquainted with the business, and the frames imperfect.”2
Once in Almy and Brown’s Pawtucket plant, Slater found the existing machinery totally unsatisfactory. He entered into a partnership with Almy and Brown to erect “perpetual card and spinning” machines, otherwise known as the Arkwright patents. By 1793, the firm of Almy, Brown and Slater was operating a seventy-two-spindle mill, producing high-quality yarn. From the Pawtucket mill, the American cotton-spinning industry was launched.
The Slater mill not only copied British technology but recreated that country’s arrangement of family labor, which included young children, six-day weeks, the minimum twelve-hour day, Sabbath schools, and payment of wages partly in goods and partly in cash. The form of ownership and management also followed British lines—one partner financed the venture, while the other furnished the technical know-how. For these accomplishments, Samuel Slater has been called “the father of American manufactures.” His story underscores the international role of textiles and apparel, their impetus in national economic development, and their place in conflicts over domestic production and imports—a theme that recurs throughout U.S. history. For example, from the outset of the new nation, President George Washington and his Secretary of the Treasury Alexander Hamilton wanted to encourage U.S.-based industry. Indeed, Washington wore a dark brown suit, entirely made in America, for his first inaugural on April 30, 1789.3
```
* input: `$ grep -i "change" ch1.txt`
* output: the command should return all the lines that contains the string **"change"** case insensitively
```
A retail-apparel-textile channel typically includes the companies that manufacture synthetic fibers; produce, gather, and refine natural fibers; spin fiber into yarn; weave or knit yarn into fabric; manufacture buttons, zippers, and other garment components; and cut and sew fabric into garments. It also includes the retailers who sell garments to end consumers. The retail link often involves services or instructions to suppliers about fabric and garment design, packaging, distribution, order fulfillment, and transportation. And it is in some of these areas, particularly distribution and order fulfillment, that channel dynamics have undergone substantial change during the last decade.
...
The information-integrated channel, with its emphasis on time and product perishability, is the basis for our cautiously optimistic—and unconventional—outlook. Even more important, the forces examined in this book provide a glimpse into processes reshaping a considerable portion of the economy. Consumers no longer line up for a special suit at a store like Bond Stores; they also expect an ever more “fashionable” array of cereal products, computers, and automobiles. As the next chapter shows, the changes now under way have their roots in new technologies, just as technical advances in transportation and communication shifted the industrial landscape at the end of the last century.
```
* `-c`: this option finds the number of lines that contains the given string. For example:(the current directory is ./written_2/non-fiction/OUP/Abernathy)
* input: `$ grep -c "change" ch1.txt`
* output: `23`
* input: `$ grep -c "since" ch1.txt`
* output: `6`
* `-l`: this options shows the files that contain the given string. For example: (the current directory is ./written_2/non-fiction/OUP/Abernathy)
* input: `$ grep -l "since" *`
* output: the command shows all the files and the lines that contains **"since"** in current directory
```
ch1.txt
ch14.txt
ch15.txt
ch2.txt
ch6.txt
ch7.txt
ch8.txt
ch9.txt
```
* input: `$ grep -l "wisdom" *`
* output: the command shows all the files and the lines that contains **"wisdom"** in current directory
```
ch1.txt
ch15.txt
```
* `-r` : this option command searches for the given string recursively in the given directory. For example: (the current directory is ./written_2/non-fiction/OUP/Abernathy)
* input: `$ grep -r "wisdom"`
* output: the command shows all the files and the lines that contains **"wisdom"** in all root directory and its subdirectories.
```
ch1.txt:In many respects, our findings defy the conventional wisdom. When we began our research, we were advised by American industry participants to establish better performance measures—for example, how many minutes does it take to make a shirt? The traditional view holds that because manufacturing performance is determined by the labor time required to produce an item, then what applies to cars, for example, can also apply to clothing; therefore, U.S. apparel manufacturers might be able to save themselves by improving assembly operations.3 Yet after years of studying hundreds of American apparel firms, we have found that direct labor content is not the primary issue. The companies that have adopted new information systems and management practices, participating in a well-integrated channel, are the ones with the strongest performance today—not those that have simply improved assembly operations.
ch1.txt:For many commentators, a book about the future of the U.S. apparel and textile industries is still an oxymoron. The conventional wisdom paints a grim picture of where these industries are headed. Low-cost labor overseas and the 
increasing penetration of imports have certainly undercut American apparel manufacturers; apparel imports grew rapidly in most categories starting in the mid-1970s. If we measure import penetration in physical units (rather than dollar 
value),12 import penetration for men’s and boys’ suits, for example, went from just 10 percent in 1973 to 43 percent by 1996. A similar expansion in imports occurred for men’s and boys’ trousers, women’s and girls’ dresses, and women’s 
slacks and shorts.13
ch1.txt:The conventional wisdom explains the industry’s decline in this way: Apparel, particularly women’s apparel, is driven by price-based competition among generally small manufacturing and contracting establishments.17 Labor costs represent a significant portion of cost for many garment categories,18 and U.S. wage levels far exceed those of competitors in countries like the People’s Republic of China and Mexico.19 Although the magnitude of these differences varies as exchange rates fluctuate, under any realistic exchange-rate scenario, the labor cost differential is sufficiently high to put U.S. manufacturers at a very significant competitive disadvantage.
ch1.txt:In later chapters about the retail revolution, inventory management, and apparel operations, we provide an in-depth look at how such new technologies have affected the related industries. For now, we present five propositions that arise from the channel perspective of this book. The conventional wisdom can no longer predict future industry dynamics or offer guideposts for private and public policies. The channel perspective, however, indicates why the demand uncertainty and risk associated with today’s apparel industry offer new opportunities for U.S. firms.
ch1.txt:The conventional wisdom holds that the basis of competitive performance for apparel manufacturers is lowest price—period. According to Martin Feldstein, then chairman of President Reagan’s Council of Economic Advisers,
ch1.txt:Yet here the conventional wisdom misses other significant measures of performance. Managers in well-integrated channels pay attention to inventory costs, inventory replenishment practices, information reliability, and time to market rather than the traditional direct costs of labor and materials alone. In fact, competitive performance is already being driven less by how a company manages its assembly operations and more by how it manages the logistics of its operations as a whole. Our study shows that an apparel manufacturer can still be successful with a traditionally organized sewing room; a firm with innovative and productive assembly operations, on the other hand, may not be competitively viable if it has not invested in information links with retailers and other changes in management practices.
ch1.txt:When it comes to international trade agreements, the conventional wisdom sounds most bleak. It leads to stark conclusions about the long-term viability of the U.S. apparel industry, even with steps taken to improve assembly-room productivity and fashion-oriented quick response. The following comment is typical:
ch15.txt:In this final chapter, we step back to survey the ways in which information-integrated channels will affect the public and private sectors. The pervasive changes arising from lean retailing challenge the conventional wisdom about the future of international trade, labor standards, employment, and even macroeconomic fluctuations. At the same time, these changes alter the nature of competitive strategy for businesses that supply lean retailers in apparel, textile, and other industries.
```
* input: `$ grep -r "bleak"`
* output: the command shows all the files and the lines that contains **"bleak"** in all root directory and its subdirectories.
```
ch1.txt:When it comes to international trade agreements, the conventional wisdom sounds most bleak. It leads to stark conclusions about the long-term viability of the U.S. apparel industry, even with steps taken to improve assembly-room productivity and fashion-oriented quick response. The following comment is typical:
ch15.txt:Indeed, rather than turning the future more bleak, the introduction and the widespread adoption of lean retailing by all participants in the retail-apparel-textile channel provides new opportunities for the textile and apparel 
industries, at least in some segments. We see a viable future for these industries—with a few caveats. These revived opportunities do not apply with equal effect to all branches of apparel or all parts of the fashion triangle. Garments 
amenable to rapid replenishment principles have the most potential for U.S. production.
```
