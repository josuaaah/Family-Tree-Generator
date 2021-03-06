## Bible Family Tree

The picture you are seeing below, is the complete family tree of every single human person mentioned in the Bible (or at least the Old Testament, because I don't see any New Testament figures in the datasets).
The words are definitely too small to see with your naked eye. Open the picture up and zoom in to admire it in its full glory.

![Full Bible Family Tree](final_tree.png)

- _Horizontal dotted lines:_ Symbolizes marriage
- _Downward-facing solid arrows:_ Symbolizes a father-son relationship
- _Downward-facing dotted arrows:_ Symbolizes a ancestor-descendant relationship

*IMPORTANT:* If you click on the picture, you might accidentally see just a blank screen. That's because the picture is too large and you are zoomed too close into a blank area of the picture. Just scroll around and you will be able to find something.

I have obtained datasets online on the [people mentioned in the Holy Bible](https://data.world/bradys/bibledata-person),
as well as the [relationships between these people](https://data.world/bradys/bibledata-personrelationship). Credits for 
the datasets should go to Brady Stephenson, who has developed them.

The Python script `family.py` crawls through the datasets and generates a string which is written into `output.txt`. 
The output is actually code for a PlantUML class diagram, which incidentally is able to create beautiful family trees.

Finally, to generate the huge family tree which is `final_tree.png`, I had to download `plantuml.jar` and run the command 
`java -DPLANTUML_LIMIT_SIZE=81920 -Xmx1024m -jar plantuml.jar output.txt` on Terminal.

I hope to eventually generate family trees for Lord of the Rings and Game of Thrones characters.
I also hope to eventually modify `family.py` such that it is able to generate family trees from any dataset available.
