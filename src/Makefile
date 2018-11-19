TARGET          = rtsp_pusher
INCLUDES        += -I.
				   
SRCS := \
	rtsp_pusher.cpp

OBJS    = $(SRCS:.cpp=.o)

%.o: %.cpp
	$(CC) $(CFLAGS) $(INCLUDES) -std=gnu++11 -c -o $@ $<

$(TARGET): $(OBJS)
	$(CC) $(LDFLAGS) $(INCLUDES) $(OBJS) $(LIBS) -o $@

all:$(TARGET) install

install:
	mkdir -p $(CONFIG_PREFIX)/usr/bin
	cp $(TARGET) $(CONFIG_PREFIX)/usr/bin

clean:
	rm -rf $(TARGET) *.o *~
