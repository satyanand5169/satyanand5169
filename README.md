- 👋 Hi, I’m @satyanand5169
- 👀 I’m interested in ...data analyst
- 🌱 I’m currently learning ...sql
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

create database project;
use project;

<!---
satyanand5169/satyanaalter table project rename column `call duration in minutes` to call_duration;
select * from project;
update project set call_timestamp =str_to_date(call_timestamp,"%m/%d/%Y");
select * from project;
update project set call_timestamp =date_format(call_timestamp,"%d-%m-%Y");
set autocommit=0;
update project set csat_score =NULL where csat_score=0;
-- find all the unique values from all column
select distinct customer_name from project; 
select distinct channel from project;
select distinct sentiment from project;
select distinct call_center from project;
select distinct city from project;
select distinct state from project;
select distinct reason from project;
select * from project;
select reason,count(*) as total_count from project group by reason order by 2 desc;
select sentiment,count(*) as total_count from project group by sentiment order by 2 desc;
select sentiment,count(*) as total_count,round((count(*)/(select count(*) from project))*100,2) as percentage from project group by sentiment order by 2 desc;
select sentiment,count(*) as total_count,round((count(*)/(select count(*) from project))*100,2) as percentage from project group by sentiment order by 2 desc;
-- negative call were around 52% where as positive calls were 22% and remaining were neutral 
select * from project;
select reason,count(*) as total_count,round((count(*)/(select count(*) from project))*100,2) as percentage from project group by reason;
select reason,count(*) as total_count,round((count(*)/(select count(*) from project))*100,1) as percentage from project group by reason;
 
 -- call for billing was about 71% where as for service outage and payments where 14% each
select channel,count(*) as total_count,round((count(*)/(select count(*) from project))*100,2) from project group by channel;
-- find the call center having maximum call
select call_center,count(*) as total_count,round((count(*)/(select count(*) from project))*100,2) from project group by call_center order by 3 desc;

-- Los Angeles got 41% of call which is highest among all the call centers
-- top 5 states-- 
select state,count(*) as total_calls from project group by state order by total_calls desc limit 5;
-- top 5 city
select city,count(*) as total_calls from project group by city order by total_calls desc limit 5;

-- to find the maximum call duration
select * from project;
select  distinct response_time,call_duration from project order by 2 desc;
-- maximum call_duration is of 45 minutes for all the response time
select  distinct sentiment,call_duration from project order by 2 desc;
-- find the top 5 customer based on csat score
select distinct customer_name,csat_score from project order by 2 desc limit 5;
-- find the top 5 customer based on call_duration
select distinct customer_name,call_duration from project order by 2 desc limit 5;

select channel,min(call_duration) as min_call_duration,max(call_duration) as max_call_duration,avg(call_duration) as avgerage_call_duration from project group by channel;

select sentiment,min(call_duration) as min_call_duration,max(call_duration) as max_call_duration,avg(call_duration) as avg_call_duration from project group by sentiment;

select reason,min(call_duration) as min_call_duration,max(call_duration) as max_call_duration,avg(call_duration) as avg_call_duration from project group by reason;

select call_center,min(call_duration) as min_call_duration,max(call_duration) as max_call_duration,avg(call_duration) as avg_call_duration from project group by call_center;

select channel,min(csat_score) as min_csat_score,max(csat_score) as max_csat_score,avg(csat_score) as avg_csat_score from project group by channel;

select sentiment,min(csat_score) as min_csat_score,max(csat_score) as max_csat_score,avg(csat_score) as avg_csat_score from project group by sentiment;

select reason,min(csat_score) as min_csat_score,max(csat_score) as max_csat_score,avg(csat_score) as avg_csat_score from project group by reason;

select call_center,min(csat_score) as min_csat_score,max(csat_score) as max_csat_score,avg(csat_score) as avg_csat_score from project group by call_center;

select year(call_timestamp),count(*) from project group by year(call_timestamp);
update project set call_timestamp =str(call_timestamp,"%m/%d/%Y");
select * from project;

update project set call_timestamp =date_format(call_timestamp,"%d-%m-%Y");

select * from project;
rollback;
update project set call_timestamp =date_format(call_timestamp,"%Y-%m-%d");

alter table project add column year varchar(100);
select * from project;
select year,sum(call_duration) from project group by year;
select year,avg(call_duration) from project group by year;
select * from project;
nd5169 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
