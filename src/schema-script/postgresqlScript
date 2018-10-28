-- Create table
create table APP_USER
(
  USER_ID           BIGINT not null,
  USER_NAME         VARCHAR(36) not null,
  ENCRYTED_PASSWORD VARCHAR(128) not null,
  LAST_LOGIN        TIMESTAMPTZ,
  LAST_LOGOUT       TIMESTAMPTZ,
  IS_ACTIVE         BOOLEAN not null
) ;

SET timezone = 'America/New_York';
--
alter table APP_USER
  add constraint APP_USER_PK primary key (USER_ID);

alter table APP_USER
  add constraint APP_USER_UK unique (USER_NAME);


-- Create table
create table APP_ROLE
(
  ROLE_ID   BIGINT not null,
  ROLE_NAME VARCHAR(30) not null
) ;
--
alter table APP_ROLE
  add constraint APP_ROLE_PK primary key (ROLE_ID);

alter table APP_ROLE
  add constraint APP_ROLE_UK unique (ROLE_NAME);


-- Create table
create table USER_ROLE
(
  ID      BIGINT not null,
  USER_ID BIGINT not null,
  ROLE_ID BIGINT not null
);
--
alter table USER_ROLE
  add constraint USER_ROLE_PK primary key (ID);

alter table USER_ROLE
  add constraint USER_ROLE_UK unique (USER_ID, ROLE_ID);

alter table USER_ROLE
  add constraint USER_ROLE_FK1 foreign key (USER_ID)
  references APP_USER (USER_ID);

alter table USER_ROLE
  add constraint USER_ROLE_FK2 foreign key (ROLE_ID)
  references APP_ROLE (ROLE_ID);



-- Used by Spring Remember Me API.
CREATE TABLE Persistent_Logins (

    username varchar(64) not null,
    series varchar(64) not null,
    token varchar(64) not null,
    last_used timestamp not null,
    PRIMARY KEY (series)

);

--------------------------------------
insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (7, 'Manager1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (6, 'Billing1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (5, 'DataProcessing1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (4, 'FileTransfer1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (3, 'Programmer1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (2, 'dbuser1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

insert into App_User (USER_ID, USER_NAME, encrypted_password, IS_ACTIVE)
values (1, 'dbadmin1', '$2a$10$PrI5Gk9L.tSZiW9FXhTS8O8Mz9E97k2FZbFvGFFaSsiTUIl.TCrFu', TRUE);

---



insert into app_role (ROLE_ID, ROLE_NAME)
values (1, 'ROLE_ADMIN');

insert into app_role (ROLE_ID, ROLE_NAME)
values (2, 'ROLE_USER');

insert into app_role (ROLE_ID, ROLE_NAME)
values (3, 'ROLE_Production_Programmer');

insert into app_role (ROLE_ID, ROLE_NAME)
values (4, 'ROLE_File_Transfer');

insert into app_role (ROLE_ID, ROLE_NAME)
values (5, 'ROLE_Data_Processing');

insert into app_role (ROLE_ID, ROLE_NAME)
values (6, 'ROLE_Billing');

insert into app_role (ROLE_ID, ROLE_NAME)
values (7, 'ROLE_Manager');


---

insert into user_role (ID, USER_ID, ROLE_ID)
values (1, 1, 1);

insert into user_role (ID, USER_ID, ROLE_ID)
values (2, 1, 2);

insert into user_role (ID, USER_ID, ROLE_ID)
values (3, 2, 2);

insert into user_role (ID, USER_ID, ROLE_ID)
values (4, 3, 3);

insert into user_role (ID, USER_ID, ROLE_ID)
values (5, 4, 4);

insert into user_role (ID, USER_ID, ROLE_ID)
values (6, 5, 5);

insert into user_role (ID, USER_ID, ROLE_ID)
values (7, 6, 6);

insert into user_role (ID, USER_ID, ROLE_ID)
values (8, 7, 7);
---
Commit;