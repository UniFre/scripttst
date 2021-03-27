$File
JpegFiles=$(find . -type f -name "*.jpeg" -not \( -name "_thumbnail"\) )
if [ -n "$File" ]
then
cat $File | while read f; do convert -resize "360x360>" $(basename "$JpegFiles" .JPG)__thumbnail.jpg; done < File
else
for file in $JpegFiles;
do
convert -resize "360x360>" $(basename "$JpegFiles" .JPG)__thumbnail.jpg
fi