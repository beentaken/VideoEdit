# VideoEdit


ffmpeg -rtsp_transport tcp -stimeout 5000000 -rtsp_flags prefer_tcp -fflags +genpts \
-i "rtsp://172.19.128.5:9090/playback?cameraid=1000279$1$0$1&begintime=1747987772&endtime=1747987788&type=2&substream=0&recordtype=1" \
-c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an \
-movflags +frag_keyframe+empty_moov -f mp4 -y output1.mp4



 ffmpeg -rtsp_transport tcp -i rtsp://xxxxx:xxxx@xxxx:xxx/Streaming/Channels/102  -c copy -movflags +frag_keyframe+empty_moov -f mp4 -y output.mp4

 ffmpeg -rtsp_transport tcp -i "rtsp://xxxxx:xxxx@xxxx:xxx/Streaming/Channels/102" ^
-c:v libx264 -preset ultrafast -tune zerolatency ^
-movflags +frag_keyframe+empty_moov -f mp4 -y output.mp4

ffmpeg -rtsp_transport tcp -i "rtsp://xxxxx:xxxx@xxxx:xxx/Streaming/Channels/102" ^
-c:v libx264 -preset ultrafast -tune zerolatency ^
-movflags +frag_keyframe+empty_moov -f mp4 -y output.mp4

ffmpeg -rtsp_transport tcp -stimeout 10000000 -i "rtsp://admin:User@123@10.128.3.1:554/Streaming/Channels/102" ^
-c:v libx264 -preset ultrafast -tune zerolatency ^
-movflags +frag_keyframe+empty_moov -f mp4 -y output.mp4

$ffmpegCommand = ".\ffmpeg1 -rtsp_transport tcp -i `"$InputPath`" -c:v libx264 -preset ultrafast -tune zerolatency -movflags +frag_keyframe+empty_moov -f mp4 -y `"$OutputPath`""



ffmpeg -rtsp_transport tcp -i "rtsp://xxxxx:xxxxxxxxxx/cam/playback?channel=1&starttime=20240521T080000Z&endtime=20240521T083000Z" ^
-c:v libx264 -preset ultrafast -tune zerolatency ^
-movflags +frag_keyframe+empty_moov -f mp4 -y output.mp4

ffprobe -rtsp_transport tcp -count_frames -select_streams v:0 -show_entries stream=nb_read_frames -print_format json rtsp://user:pass@ip:port/stream

[25-05-26 10:12:55.528 INF] [ERR] frame=  139 fps= 13 q=20.0 size=       0KiB time=00:00:09.26 bitrate=   0.0kbits/s dup=0 drop=3 speed=0.856x    
[25-05-26 10:12:56.043 INF] [ERR] frame=  139 fps= 12 q=20.0 size=       0KiB time=00:00:09.26 bitrate=   0.0kbits/s dup=0 drop=3 speed=0.817x    
[25-05-26 10:12:56.559 INF] [ERR] frame=  139 fps= 12 q=20.0 size=       0KiB time=00:00:09.26 bitrate=   0.0kbits/s dup=0 drop=3 speed=0.782x 

ffmpeg -i input -c:v libx264 -preset fast -crf 23 -tag:v avc1 -c:a aac -b:a 128k -movflags +faststart output.mp4

-rtsp_transport tcp -i \"{rtspUrl}\" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -t {duration.Value.TotalSeconds} -movflags +frag_keyframe+empty_moov+faststart -f mp4 -y "\"
{outputPath}\"

ffmpeg -rtsp_transport tcp -i "rtsp://xxxxx:9090/playback?cameraid=xxxxx$1$0$1&begintime=1747987777&endtime=1747987788&type=2&substream=0&recordtype=1" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -movflags +frag_keyframe+empty_moov -f mp4 -y output1.mp4

string arguments = $"-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i \"{rtspUrl}\" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -movflags +frag_keyframe+empty_moov+default_base_moof -f mp4 -flush_packets 1 -y \"{outputPath}\"";

-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i "rtsp://xxxxx:9090/playback?cameraid=1000008$1$0$57&begintime=1748424451&endtime=1748424467&type=2&substream=0&recordtype=1" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -movflags +frag_keyframe+empty_moov+default_base_moof -f mp4 -flush_packets 1 -y "a.mp4"

string arguments = $"-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i \"{rtspUrl}\" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -f hls -hls_time 2 -hls_list_size 10 -hls_flags delete_segments \"{outputPath.Replace(".mp4", ".m3u8")}\"";

-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i "rtsp://xxxxx:9090/playback?cameraid=1000008$1$0$57&begintime=1748424451&endtime=1748424467&type=2&substream=0&recordtype=1" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -f hls -hls_time 2 -hls_list_size 10 -hls_flags delete_segments "b.mp4"

string arguments = $"-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i \"{rtspUrl}\" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -movflags +frag_keyframe+empty_moov+default_base_moof -frag_duration 1000000 -f mp4 -flush_packets 1 -y \"{rtspUrl}\"";

-rtsp_transport tcp -rtsp_flags prefer_tcp -fflags +genpts -i "rtsp://xxxxx:9090/playback?cameraid=1000008$1$0$57&begintime=1748424451&endtime=1748424467&type=2&substream=0&recordtype=1" -c:v libx264 -preset ultrafast -tune zerolatency -crf 30 -g 50 -pix_fmt yuv420p -an -movflags +frag_keyframe+empty_moov+default_base_moof -frag_duration 1000000 -f mp4 -flush_packets 1 -y "c.mp4"
