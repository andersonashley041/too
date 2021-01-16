

   QOMX_COLOR_FormatYUV420PackedSemiPlanar64x32Tile2m8ka.
 * First wtf: why call it YUV420? It is NV12 (interleaved U&V).
@@ -42,8 +34,7 @@
#define TILE_SIZE (TILE_WIDTH * TILE_HEIGHT)
 
/* get frame tile coordinate. XXX: nothing to be understood here, don't try. */
-static size_t tile_pos(size_t x, size_t y, size_t w, size_t h)
-{
+static size_t tile_pos(size_t x, size_t y, size_t w, size_t h) {
    size_t flim = x + (y & ~1) * w;
 
    if (y & 1) {
@@ -55,11 +46,10 @@
    return flim;
}
