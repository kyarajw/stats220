reject <- image_read('https://media.istockphoto.com/id/1356060337/photo/young-man-refusing-your-offer.jpg?s=612x612&w=0&k=20&c=Wx3t-aX5q3MjjzBhnwpK7-W16i-SRiDy75M_els_pYQ=') %>%
    image_scale(500)
lazing <- image_annotate(image_blank(width = 500, height = 500, color = '#FFFFFF'), text = "Lazing\naround", color = '#000000', size = 80, gravity = 'center')
top_row = c(reject, lazing) %>%
image_append()

consider <- image_scale(image_read('https://media.istockphoto.com/id/1464159103/photo/thoughtful-woman-with-hand-on-chin-looking-up.jpg?s=612x612&w=0&k=20&c=9CxJYoqv3GTKhDy06Qwx5pFaS5faaA2JJSUAB1m3S58='), 500)
napping <- image_annotate(image_blank(color = '#FFFFFF', width = 500, height = 500), text = 'Napping', gravity = 'center', size = 80, color = '#000000')
middle = c(consider, napping) %>%
image_append()

agree <- image_scale(image_read('https://cdn.pixabay.com/photo/2017/06/09/05/21/ok-2385794_1280.jpg'), 500)
conserving_energy <- image_annotate(image_blank(color = '#FFFFFF', width = 500, height = 500), text = "Conserving\nenergy", size = 80, gravity = 'center', color = '#000000')
bottom = c(agree, conserving_energy) %>%
image_append()

c(top_row, middle, bottom) %>%
image_append(stack = TRUE)
