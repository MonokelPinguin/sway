include_directories(
	${PROTOCOLS_INCLUDE_DIRS}
	${PANGO_INCLUDE_DIRS}
	${GDK_PIXBUF_INCLUDE_DIRS}
	${XKBCOMMON_INCLUDE_DIRS}
)

add_library(sway-wayland
	buffers.c
	pango.c
	registry.c
	window.c
	cairo.c
	)

target_link_libraries(sway-wayland
	sway-common
	sway-protocols
	${PANGO_LIBRARIES}
	${GDK_PIXBUF_LIBRARIES}
	${XKBCOMMON_LIBRARIES}
	)
