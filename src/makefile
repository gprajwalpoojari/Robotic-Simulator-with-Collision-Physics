bmp: bmp.c
		gcc	-o	$@	$^	-std=c11

image_server:	image_server.c	bmp.c
		gcc	-o	$@	$^	-std=c11	-lpthread

rasterize:	rasterize.c	bmp.c	image_server.c	vector_xy_i32_t.c vector_xy_t.c graphics.c
		gcc -o	$@	$^	-std=c11	-lpthread	-lm

braitenberg:	braitenberg.c	bmp.c	image_server.c	vector_xy_i32_t.c vector_xy_t.c graphics.c collision.c
		gcc -o	$@	$^	-std=c11	-lpthread	-lm
