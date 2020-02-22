SELECT SQL_CALC_FOUND_ROWS video_id from el_zy_order_course where uid=1082 GROUP BY video_id limit 0,10;
SELECT FOUND_ROWS() as count;