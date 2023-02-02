# MARVL-transcripts
Process transcripts from Youtube and other paid services (Otter.AI and possibly Fireflies.ai in the future).

Content: 
- [`raw`](raw): TXT files with transcripts from different sales-related videos. 
- [`notebooks`](notebooks): notebook with quick EDA and function to clean transcript files and format them in appropriate CSV format.
- [`output`](output): CSV files with formatted data. 

# Youtube transcripts
To generate transcripts using Youtube, it's not necessary to download the video. The transcript can be generated automatically by going to the video and opening the options menu. The issue with this is that there is no distinction between speakers. The quality may also not be as high as in other specialized apps for video transcription.

# Transcripts from paid services
In this case, the transcript shows different paragraphs for different speakers. While this is a nice feature, it's not guaranteed that we need it, so confirmation is needed to avoid paying for a premium service we may not need.

# Data processing
Since the transcripts follow the format below, formatting of the data can be done by loading everything into a Pandas DataFrame and then selecting slices to format.

```
# Youtube format
timestamp1
sentence1
timestamp2
sentence2
...

# Otter.AI format
timestamp1
sentence1
\n
timestamp2
sentence2
